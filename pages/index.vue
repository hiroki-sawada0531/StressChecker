<template>
  <div class="container">
    <div id="allPages">
      <div v-show="page === 1" class="selection" id="page-1">
        <h1>ストレス診断</h1>
        <h2>Ａ あなたの仕事についてうかがいます。最もあてはまるものにチェックを入れてください。</h2>
        <p id="question_a_1">
            1. 非常にたくさんの仕事をしなければならない<br>
            <input v-model="question_a_1" type="radio" name="question_a_1" value=4>そうだ<br>
            <input v-model="question_a_1" type="radio" name="question_a_1" value=3>まあそうだ<br>
            <input v-model="question_a_1" type="radio" name="question_a_1" value=2>ややちがう<br>
            <input v-model="question_a_1" type="radio" name="question_a_1" value=1>ちがう<br>
        </p>
        <p id="question_a_2">
            2. 時間内に仕事が処理しきれない<br>
            <input v-model="question_a_2" type="radio" name="question_a_2" value=4>そうだ<br>
            <input v-model="question_a_2" type="radio" name="question_a_2" value=3>まあそうだ<br>
            <input v-model="question_a_2" type="radio" name="question_a_2" value=2>ややちがう<br>
            <input v-model="question_a_2" type="radio" name="question_a_2" value=1>ちがう<br>
        </p>
        <p id="question_a_3">
            3. 一生懸命働かなければならない<br>
            <input v-model="question_a_3" type="radio" name="question_a_3" value=1>そうだ<br>
            <input v-model="question_a_3" type="radio" name="question_a_3" value=2>まあそうだ<br>
            <input v-model="question_a_3" type="radio" name="question_a_3" value=3>ややちがう<br>
            <input v-model="question_a_3" type="radio" name="question_a_3" value=4>ちがう<br>
        </p>
        <p id="question_a_4">
            4. かなり注意を集中する必要がある<br>
            <input v-model="question_a_4" type="radio" name="question_a_4" value=4>そうだ<br>
            <input v-model="question_a_4" type="radio" name="question_a_4" value=3>まあそうだ<br>
            <input v-model="question_a_4" type="radio" name="question_a_4" value=2>ややちがう<br>
            <input v-model="question_a_4" type="radio" name="question_a_4" value=1>ちがう<br>
        </p>
        <p id="question_a_5">
            5. 高度の知識や技術が必要なむずかしい仕事だ<br>
            <input v-model="question_a_5" type="radio" name="question_a_5" value=4>そうだ<br>
            <input v-model="question_a_5" type="radio" name="question_a_5" value=3>まあそうだ<br>
            <input v-model="question_a_5" type="radio" name="question_a_5" value=2>ややちがう<br>
            <input v-model="question_a_5" type="radio" name="question_a_5" value=1>ちがう<br>
        </p>
        <p id="question_a_6">
            6. 勤務時間中はいつも仕事のことを考えていなければならない<br>
            <input v-model="question_a_6" type="radio" name="question_a_6" value=1>そうだ<br>
            <input v-model="question_a_6" type="radio" name="question_a_6" value=2>まあそうだ<br>
            <input v-model="question_a_6" type="radio" name="question_a_6" value=3>ややちがう<br>
            <input v-model="question_a_6" type="radio" name="question_a_6" value=4>ちがう<br>
        </p>
        <p id="question_a_7">
            7. からだを大変よく使う仕事だ<br>
            <input v-model="question_a_7" type="radio" name="question_a_7" value=4>そうだ<br>
            <input v-model="question_a_7" type="radio" name="question_a_7" value=3>まあそうだ<br>
            <input v-model="question_a_7" type="radio" name="question_a_7" value=2>ややちがう<br>
            <input v-model="question_a_7" type="radio" name="question_a_7" value=1>ちがう<br>
        </p>
        <p id="question_a_8">
            8. 自分のペースで仕事ができる<br>
            <input v-model="question_a_8" type="radio" name="question_a_8" value=1>そうだ<br>
            <input v-model="question_a_8" type="radio" name="question_a_8" value=2>まあそうだ<br>
            <input v-model="question_a_8" type="radio" name="question_a_8" value=3>ややちがう<br>
            <input v-model="question_a_8" type="radio" name="question_a_8" value=4>ちがう<br>
        </p>
        <p id="question_a_9">
            9. 自分で仕事の順番・やり方を決めることができる<br>
            <input v-model="question_a_9" type="radio" name="question_a_9" value=1>そうだ<br>
            <input v-model="question_a_9" type="radio" name="question_a_9" value=2>まあそうだ<br>
            <input v-model="question_a_9" type="radio" name="question_a_9" value=3>ややちがう<br>
            <input v-model="question_a_9" type="radio" name="question_a_9" value=4>ちがう<br>
        </p>
        <p id="question_a_10">
            10. 職場の仕事の方針に自分の意見を反映できる<br>
            <input v-model="question_a_10" type="radio" name="question_a_10" value=1>そうだ<br>
            <input v-model="question_a_10" type="radio" name="question_a_10" value=2>まあそうだ<br>
            <input v-model="question_a_10" type="radio" name="question_a_10" value=3>ややちがう<br>
            <input v-model="question_a_10" type="radio" name="question_a_10" value=4>ちがう<br>
        </p>
        <p id="question_a_11">
            11. 自分の技能や知識を仕事で使うことが少ない<br>
            <input v-model="question_a_11" type="radio" name="question_a_11" value=4>そうだ<br>
            <input v-model="question_a_11" type="radio" name="question_a_11" value=3>まあそうだ<br>
            <input v-model="question_a_11" type="radio" name="question_a_11" value=2>ややちがう<br>
            <input v-model="question_a_11" type="radio" name="question_a_11" value=1>ちがう<br>
        </p>
        <p id="question_a_12">
            12. 私の部署内で意見のくい違いがある<br>
            <input v-model="question_a_12" type="radio" name="question_a_12" value=4>そうだ<br>
            <input v-model="question_a_12" type="radio" name="question_a_12" value=3>まあそうだ<br>
            <input v-model="question_a_12" type="radio" name="question_a_12" value=2>ややちがう<br>
            <input v-model="question_a_12" type="radio" name="question_a_12" value=1>ちがう<br>
        </p>
        <p id="question_a_13">
            13. 私の部署と他の部署とはうまが合わない<br>
            <input v-model="question_a_13" type="radio" name="question_a_13" value=4>そうだ<br>
            <input v-model="question_a_13" type="radio" name="question_a_13" value=3>まあそうだ<br>
            <input v-model="question_a_13" type="radio" name="question_a_13" value=2>ややちがう<br>
            <input v-model="question_a_13" type="radio" name="question_a_13" value=1>ちがう<br>
        </p>
        <p id="question_a_14">
            14. 私の職場の雰囲気は友好的である<br>
            <input v-model="question_a_14" type="radio" name="question_a_14" value=1>そうだ<br>
            <input v-model="question_a_14" type="radio" name="question_a_14" value=2>まあそうだ<br>
            <input v-model="question_a_14" type="radio" name="question_a_14" value=3>ややちがう<br>
            <input v-model="question_a_14" type="radio" name="question_a_14" value=4>ちがう<br>
        </p>
        <p id="question_a_15">
            15. 私の職場の作業環境（騒音、照明、温度、換気など）はよくない<br>
            <input v-model="question_a_15" type="radio" name="question_a_15" value=4>そうだ<br>
            <input v-model="question_a_15" type="radio" name="question_a_15" value=3>まあそうだ<br>
            <input v-model="question_a_15" type="radio" name="question_a_15" value=2>ややちがう<br>
            <input v-model="question_a_15" type="radio" name="question_a_15" value=1>ちがう<br>
        </p>
        <p id="question_a_16">
            16. 仕事の内容は自分にあっている<br>
            <input v-model="question_a_16" type="radio" name="question_a_16" value=1>そうだ<br>
            <input v-model="question_a_16" type="radio" name="question_a_16" value=2>まあそうだ<br>
            <input v-model="question_a_16" type="radio" name="question_a_16" value=3>ややちがう<br>
            <input v-model="question_a_16" type="radio" name="question_a_16" value=4>ちがう<br>
        </p>
        <p id="question_a_17">
            17. 働きがいのある仕事だ<br>
            <input v-model="question_a_17" type="radio" name="question_a_17" value=1>そうだ<br>
            <input v-model="question_a_17" type="radio" name="question_a_17" value=2>まあそうだ<br>
            <input v-model="question_a_17" type="radio" name="question_a_17" value=3>ややちがう<br>
            <input v-model="question_a_17" type="radio" name="question_a_17" value=4>ちがう<br>
        </p>
        <div @click="next">- 次へ -</div>
      </div>
      <div v-show="page === 2" class="selection" id="page-2">
        <h2>Ｂ 最近 1 か月間のあなたの状態についてうかがいます。最もあてはまるものにチェックを入れてください。</h2>
        <p id="question_b_1">
            1. 活気がわいてくる<br>
            <input v-model="question_b_1" type="radio" name="question_b_1" value=4>ほとんどなかった<br>
            <input v-model="question_b_1" type="radio" name="question_b_1" value=3>ときどきあった<br>
            <input v-model="question_b_1" type="radio" name="question_b_1" value=2>しばしばあった<br>
            <input v-model="question_b_1" type="radio" name="question_b_1" value=1>ほとんどいつもあった<br>
        </p>
        <p id="question_b_2">
            2. 元気がいっぱいだ<br>
            <input v-model="question_b_2" type="radio" name="question_b_2" value=4>ほとんどなかった<br>
            <input v-model="question_b_2" type="radio" name="question_b_2" value=3>ときどきあった<br>
            <input v-model="question_b_2" type="radio" name="question_b_2" value=2>しばしばあった<br>
            <input v-model="question_b_2" type="radio" name="question_b_2" value=1>ほとんどいつもあった<br>
        </p>
        <p id="question_b_3">
            3. 生き生きする<br>
            <input v-model="question_b_3" type="radio" name="question_b_3" value=4>ほとんどなかった<br>
            <input v-model="question_b_3" type="radio" name="question_b_3" value=3>ときどきあった<br>
            <input v-model="question_b_3" type="radio" name="question_b_3" value=2>しばしばあった<br>
            <input v-model="question_b_3" type="radio" name="question_b_3" value=1>ほとんどいつもあった<br>
        </p>
        <p id="question_b_4">
            4. 怒りを感じる<br>
            <input v-model="question_b_4" type="radio" name="question_b_4" value=1>ほとんどなかった<br>
            <input v-model="question_b_4" type="radio" name="question_b_4" value=2>ときどきあった<br>
            <input v-model="question_b_4" type="radio" name="question_b_4" value=3>しばしばあった<br>
            <input v-model="question_b_4" type="radio" name="question_b_4" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_5">
            5. 内心腹立たしい<br>
            <input v-model="question_b_5" type="radio" name="question_b_5" value=1>ほとんどなかった<br>
            <input v-model="question_b_5" type="radio" name="question_b_5" value=2>ときどきあった<br>
            <input v-model="question_b_5" type="radio" name="question_b_5" value=3>しばしばあった<br>
            <input v-model="question_b_5" type="radio" name="question_b_5" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_6">
            6. イライラしている<br>
            <input v-model="question_b_6" type="radio" name="question_b_6" value=1>ほとんどなかった<br>
            <input v-model="question_b_6" type="radio" name="question_b_6" value=2>ときどきあった<br>
            <input v-model="question_b_6" type="radio" name="question_b_6" value=3>しばしばあった<br>
            <input v-model="question_b_6" type="radio" name="question_b_6" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_7">
            7. ひどく疲れた<br>
            <input v-model="question_b_7" type="radio" name="question_b_7" value=1>ほとんどなかった<br>
            <input v-model="question_b_7" type="radio" name="question_b_7" value=2>ときどきあった<br>
            <input v-model="question_b_7" type="radio" name="question_b_7" value=3>しばしばあった<br>
            <input v-model="question_b_7" type="radio" name="question_b_7" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_8">
            8. へとへとだ<br>
            <input v-model="question_b_8" type="radio" name="question_b_8" value=1>ほとんどなかった<br>
            <input v-model="question_b_8" type="radio" name="question_b_8" value=2>ときどきあった<br>
            <input v-model="question_b_8" type="radio" name="question_b_8" value=3>しばしばあった<br>
            <input v-model="question_b_8" type="radio" name="question_b_8" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_9">
            9. だるい<br>
            <input v-model="question_b_9" type="radio" name="question_b_9" value=1>ほとんどなかった<br>
            <input v-model="question_b_9" type="radio" name="question_b_9" value=2>ときどきあった<br>
            <input v-model="question_b_9" type="radio" name="question_b_9" value=3>しばしばあった<br>
            <input v-model="question_b_9" type="radio" name="question_b_9" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_10">
            10. 気がはりつめている<br>
            <input v-model="question_b_10" type="radio" name="question_b_10" value=1>ほとんどなかった<br>
            <input v-model="question_b_10" type="radio" name="question_b_10" value=2>ときどきあった<br>
            <input v-model="question_b_10" type="radio" name="question_b_10" value=3>しばしばあった<br>
            <input v-model="question_b_10" type="radio" name="question_b_10" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_11">
            11. 不安だ<br>
            <input v-model="question_b_11" type="radio" name="question_b_11" value=1>ほとんどなかった<br>
            <input v-model="question_b_11" type="radio" name="question_b_11" value=2>ときどきあった<br>
            <input v-model="question_b_11" type="radio" name="question_b_11" value=3>しばしばあった<br>
            <input v-model="question_b_11" type="radio" name="question_b_11" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_12">
            12. 落着かない<br>
            <input v-model="question_b_12" type="radio" name="question_b_12" value=1>ほとんどなかった<br>
            <input v-model="question_b_12" type="radio" name="question_b_12" value=2>ときどきあった<br>
            <input v-model="question_b_12" type="radio" name="question_b_12" value=3>しばしばあった<br>
            <input v-model="question_b_12" type="radio" name="question_b_12" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_13">
            13. ゆううつだ<br>
            <input v-model="question_b_13" type="radio" name="question_b_13" value=1>ほとんどなかった<br>
            <input v-model="question_b_13" type="radio" name="question_b_13" value=2>ときどきあった<br>
            <input v-model="question_b_13" type="radio" name="question_b_13" value=3>しばしばあった<br>
            <input v-model="question_b_13" type="radio" name="question_b_13" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_14">
            14. 何をするのも面倒だ<br>
            <input v-model="question_b_14" type="radio" name="question_b_14" value=1>ほとんどなかった<br>
            <input v-model="question_b_14" type="radio" name="question_b_14" value=2>ときどきあった<br>
            <input v-model="question_b_14" type="radio" name="question_b_14" value=3>しばしばあった<br>
            <input v-model="question_b_14" type="radio" name="question_b_14" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_15">
            15. 物事に集中できない<br>
            <input v-model="question_b_15" type="radio" name="question_b_15" value=1>ほとんどなかった<br>
            <input v-model="question_b_15" type="radio" name="question_b_15" value=2>ときどきあった<br>
            <input v-model="question_b_15" type="radio" name="question_b_15" value=3>しばしばあった<br>
            <input v-model="question_b_15" type="radio" name="question_b_15" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_16">
            16. 気分が晴れない<br>
            <input v-model="question_b_16" type="radio" name="question_b_16" value=1>ほとんどなかった<br>
            <input v-model="question_b_16" type="radio" name="question_b_16" value=2>ときどきあった<br>
            <input v-model="question_b_16" type="radio" name="question_b_16" value=3>しばしばあった<br>
            <input v-model="question_b_16" type="radio" name="question_b_16" value=4>ほとんどいつもあった<br>
        </p>
<!-- kokokara -->
        <p id="question_b_17">
            17. 仕事が手につかない<br>
            <input v-model="question_b_17" type="radio" name="question_b_17" value=1>ほとんどなかった<br>
            <input v-model="question_b_17" type="radio" name="question_b_17" value=2>ときどきあった<br>
            <input v-model="question_b_17" type="radio" name="question_b_17" value=3>しばしばあった<br>
            <input v-model="question_b_17" type="radio" name="question_b_17" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_18">
            18. 悲しいと感じる<br>
            <input v-model="question_b_18" type="radio" name="question_b_18" value=1>ほとんどなかった<br>
            <input v-model="question_b_18" type="radio" name="question_b_18" value=2>ときどきあった<br>
            <input v-model="question_b_18" type="radio" name="question_b_18" value=3>しばしばあった<br>
            <input v-model="question_b_18" type="radio" name="question_b_18" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_19">
            19. めまいがする<br>
            <input v-model="question_b_19" type="radio" name="question_b_19" value=1>ほとんどなかった<br>
            <input v-model="question_b_19" type="radio" name="question_b_19" value=2>ときどきあった<br>
            <input v-model="question_b_19" type="radio" name="question_b_19" value=3>しばしばあった<br>
            <input v-model="question_b_19" type="radio" name="question_b_19" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_20">
            20. 体のふしぶしが痛む<br>
            <input v-model="question_b_20" type="radio" name="question_b_20" value=1>ほとんどなかった<br>
            <input v-model="question_b_20" type="radio" name="question_b_20" value=2>ときどきあった<br>
            <input v-model="question_b_20" type="radio" name="question_b_20" value=3>しばしばあった<br>
            <input v-model="question_b_20" type="radio" name="question_b_20" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_21">
            21. 頭が重かったり頭痛がする<br>
            <input v-model="question_b_21" type="radio" name="question_b_21" value=1>ほとんどなかった<br>
            <input v-model="question_b_21" type="radio" name="question_b_21" value=2>ときどきあった<br>
            <input v-model="question_b_21" type="radio" name="question_b_21" value=3>しばしばあった<br>
            <input v-model="question_b_21" type="radio" name="question_b_21" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_22">
            22. 首筋や肩がこる<br>
            <input v-model="question_b_22" type="radio" name="question_b_22" value=1>ほとんどなかった<br>
            <input v-model="question_b_22" type="radio" name="question_b_22" value=2>ときどきあった<br>
            <input v-model="question_b_22" type="radio" name="question_b_22" value=3>しばしばあった<br>
            <input v-model="question_b_22" type="radio" name="question_b_22" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_23">
            23. 腰が痛い<br>
            <input v-model="question_b_23" type="radio" name="question_b_23" value=1>ほとんどなかった<br>
            <input v-model="question_b_23" type="radio" name="question_b_23" value=2>ときどきあった<br>
            <input v-model="question_b_23" type="radio" name="question_b_23" value=3>しばしばあった<br>
            <input v-model="question_b_23" type="radio" name="question_b_23" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_24">
            24. 目が疲れる<br>
            <input v-model="question_b_24" type="radio" name="question_b_24" value=1>ほとんどなかった<br>
            <input v-model="question_b_24" type="radio" name="question_b_24" value=2>ときどきあった<br>
            <input v-model="question_b_24" type="radio" name="question_b_24" value=3>しばしばあった<br>
            <input v-model="question_b_24" type="radio" name="question_b_24" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_25">
            25. 動悸や息切れがする<br>
            <input v-model="question_b_25" type="radio" name="question_b_25" value=1>ほとんどなかった<br>
            <input v-model="question_b_25" type="radio" name="question_b_25" value=2>ときどきあった<br>
            <input v-model="question_b_25" type="radio" name="question_b_25" value=3>しばしばあった<br>
            <input v-model="question_b_25" type="radio" name="question_b_25" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_26">
            26. 胃腸の具合が悪い<br>
            <input v-model="question_b_26" type="radio" name="question_b_26" value=1>ほとんどなかった<br>
            <input v-model="question_b_26" type="radio" name="question_b_26" value=2>ときどきあった<br>
            <input v-model="question_b_26" type="radio" name="question_b_26" value=3>しばしばあった<br>
            <input v-model="question_b_26" type="radio" name="question_b_26" value=4>ほとんどいつもあった<br>
        </p>
        <p id="question_b_27">
            27. 食欲がない<br>
            <input v-model="question_b_27" type="radio" name="question_b_27" value=1>ほとんどなかった<br>
            <input v-model="question_b_27" type="radio" name="question_b_27" value=2>ときどきあった<br>
            <input v-model="question_b_27" type="radio" name="question_b_27" value=3>しばしばあった<br>
            <input v-model="question_b_27" type="radio" name="question_b_27" value=4>ほとんどいつもあった<br>
        </p>
        <p p id="question_b_28">
            28. 便秘や下痢をする<br>
            <input v-model="question_b_28" type="radio" name="question_b_28" value=1>ほとんどなかった<br>
            <input v-model="question_b_28" type="radio" name="question_b_28" value=2>ときどきあった<br>
            <input v-model="question_b_28" type="radio" name="question_b_28" value=3>しばしばあった<br>
            <input v-model="question_b_28" type="radio" name="question_b_28" value=4>ほとんどいつもあった<br>
        </p>
        <p p id="question_b_29">
            29. よく眠れない<br>
            <input v-model="question_b_29" type="radio" name="question_b_29" value=1>ほとんどなかった<br>
            <input v-model="question_b_29" type="radio" name="question_b_29" value=2>ときどきあった<br>
            <input v-model="question_b_29" type="radio" name="question_b_29" value=3>しばしばあった<br>
            <input v-model="question_b_29" type="radio" name="question_b_29" value=4>ほとんどいつもあった<br>
        </p>
        <div @click="next">- 次へ -</div>
        <div @click="prev">- 前へ -</div>
      </div>
      <div v-show="page === 3" class="selection" id="page-3">
        <h2>Ｃ あなたの周りの方々についてうかがいます。最もあてはまるものにチェックを入れてください。</h2>
        <h4>次の人たちはどのくらい気軽に話ができますか？</h4>
        <p id="question_c_1">
            1. 上司<br>
            <input v-model="question_c_1" type="radio" name="question_c_1" value=1>非常に<br>
            <input v-model="question_c_1" type="radio" name="question_c_1" value=2>かなり<br>
            <input v-model="question_c_1" type="radio" name="question_c_1" value=3>多少<br>
            <input v-model="question_c_1" type="radio" name="question_c_1" value=4>全くない<br>
        </p>
        <p id="question_c_2">
            2. 職場の同僚<br>
            <input v-model="question_c_2" type="radio" name="question_c_2" value=1>非常に<br>
            <input v-model="question_c_2" type="radio" name="question_c_2" value=2>かなり<br>
            <input v-model="question_c_2" type="radio" name="question_c_2" value=3>多少<br>
            <input v-model="question_c_2" type="radio" name="question_c_2" value=4>全くない<br>
        </p>
        <p id="question_c_3">
            3. 配偶者、家族、友人等<br>
            <input v-model="question_c_3" type="radio" name="question_c_3" value=1>非常に<br>
            <input v-model="question_c_3" type="radio" name="question_c_3" value=2>かなり<br>
            <input v-model="question_c_3" type="radio" name="question_c_3" value=3>多少<br>
            <input v-model="question_c_3" type="radio" name="question_c_3" value=4>全くない<br>
        </p>
        <h4>あなたが困った時、次の人たちはどのくらい頼りになりますか？</h4>
        <p id="question_c_4">
            1. 上司<br>
            <input v-model="question_c_4" type="radio" name="question_c_4" value=1>非常に<br>
            <input v-model="question_c_4" type="radio" name="question_c_4" value=2>かなり<br>
            <input v-model="question_c_4" type="radio" name="question_c_4" value=3>多少<br>
            <input v-model="question_c_4" type="radio" name="question_c_4" value=4>全くない<br>
        </p>
        <p id="question_c_5">
            2. 職場の同僚<br>
            <input v-model="question_c_5" type="radio" name="question_c_5" value=1>非常に<br>
            <input v-model="question_c_5" type="radio" name="question_c_5" value=2>かなり<br>
            <input v-model="question_c_5" type="radio" name="question_c_5" value=3>多少<br>
            <input v-model="question_c_5" type="radio" name="question_c_5" value=4>全くない<br>
        </p>
        <p id="question_c_6">
            3. 配偶者、家族、友人等<br>
            <input v-model="question_c_6" type="radio" name="question_c_6" value=1>非常に<br>
            <input v-model="question_c_6" type="radio" name="question_c_6" value=2>かなり<br>
            <input v-model="question_c_6" type="radio" name="question_c_6" value=3>多少<br>
            <input v-model="question_c_6" type="radio" name="question_c_6" value=4>全くない<br>
        </p>
        <h4>あなたの個人的な問題を相談したら、次の人たちはどのくらいきいてくれますか？</h4>
        <p id="question_c_7">
            1. 上司<br>
            <input v-model="question_c_7" type="radio" name="question_c_7" value=1>非常に<br>
            <input v-model="question_c_7" type="radio" name="question_c_7" value=2>かなり<br>
            <input v-model="question_c_7" type="radio" name="question_c_7" value=3>多少<br>
            <input v-model="question_c_7" type="radio" name="question_c_7" value=4>全くない<br>
        </p>
        <p id="question_c_8">
            2. 職場の同僚<br>
            <input v-model="question_c_8" type="radio" name="question_c_8" value=1>非常に<br>
            <input v-model="question_c_8" type="radio" name="question_c_8" value=2>かなり<br>
            <input v-model="question_c_8" type="radio" name="question_c_8" value=3>多少<br>
            <input v-model="question_c_8" type="radio" name="question_c_8" value=4>全くない<br>
        </p>
        <p id="question_c_9">
            3. 配偶者、家族、友人等<br>
            <input v-model="question_c_9" type="radio" name="question_c_9" value=1>非常に<br>
            <input v-model="question_c_9" type="radio" name="question_c_9" value=2>かなり<br>
            <input v-model="question_c_9" type="radio" name="question_c_9" value=3>多少<br>
            <input v-model="question_c_9" type="radio" name="question_c_9" value=4>全くない<br>
        </p>
        <div @click="prev">- 前へ -</div>
        <div @click="result">診断する</div>
        <br>
        <br>
      </div>
      <div v-show="page === 4">
        あなたの結果は、{{ totalText }} です。
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      page: 1,
      totalText: '',
      result_a: 0,
      result_b: 0,
      result_c: 0,
      question_a_0: 0,
      question_b_0: 0,
      question_c_0: 0,
      question_a_1: 0,
      question_a_2: 0,
      question_a_3: 0,
      question_a_4: 0,
      question_a_5: 0,
      question_a_6: 0,
      question_a_7: 0,
      question_a_8: 0,
      question_a_9: 0,
      question_a_10: 0,
      question_a_11: 0,
      question_a_12: 0,
      question_a_13: 0,
      question_a_14: 0,
      question_a_15: 0,
      question_a_16: 0,
      question_a_17: 0,
      question_b_1: 0, // ここからb
      question_b_2: 0,
      question_b_3: 0,
      question_b_4: 0,
      question_b_5: 0,
      question_b_6: 0,
      question_b_7: 0,
      question_b_8: 0,
      question_b_9: 0,
      question_b_10: 0,
      question_b_11: 0,
      question_b_12: 0,
      question_b_13: 0,
      question_b_14: 0,
      question_b_15: 0,
      question_b_16: 0,
      question_b_17: 0,
      question_b_18: 0,
      question_b_19: 0,
      question_b_20: 0,
      question_b_21: 0,
      question_b_22: 0,
      question_b_23: 0,
      question_b_24: 0,
      question_b_25: 0,
      question_b_26: 0,
      question_b_27: 0,
      question_b_28: 0,
      question_b_29: 0,
      question_c_1: 0, // ここからc
      question_c_2: 0,
      question_c_3: 0,
      question_c_4: 0,
      question_c_5: 0,
      question_c_6: 0,
      question_c_7: 0,
      question_c_8: 0,
      question_c_9: 0,
      result_a_1_2_3: 0, // ここからa結果
      result_a_4_5_6: 0,
      result_a_7: 0,
      result_a_12_13_14: 0,
      result_a_15: 0,
      result_a_8_9_10: 0,
      result_a_11: 0,
      result_a_16: 0,
      result_a_17: 0,
      result_b_1_2_3: 0, // ここからb結果
      result_b_4_5_6: 0,
      result_b_7_8_9: 0,
      result_a_8_9_10: 0,
      result_b_13_14_15_16_17_18: 0,
      result_b_19_20_21_22_23_24_25_26_27_28_29: 0,
      result_c_1_4_7: 0, // ここからc結果
      result_c_2_5_8: 0,
      result_c_3_6_9: 0,
    }
  },
  methods: {
    next() {
      this.page += 1
    },
    prev() {
      this.page -= 1
    },
    result() {
      // 質問a 1~17問
      this.result_a_1_2_3 = 15 - (Number(this.question_a_1) + Number(this.question_a_2) + Number(this.question_a_3))
      if (this.result_a_1_2_3 >= 3 && this.result_a_1_2_3 <= 5) {
        this.result_a += 5
      } else if (this.result_a_1_2_3 >= 6 && this.result_a_1_2_3 <= 7) {
        this.result_a += 4
      } else if (this.result_a_1_2_3 >= 8 && this.result_a_1_2_3 <= 9) {
        this.result_a += 3
      } else if (this.result_a_1_2_3 >= 10 && this.result_a_1_2_3 <= 11) {
        this.result_a += 2
      } else if (this.result_a_1_2_3 === 12) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion1か2か3がクリック出来てません！')
      }

      this.result_a_4_5_6 = 15 - (Number(this.question_a_4) + Number(this.question_a_5) + Number(this.question_a_6))
      if (this.result_a_4_5_6 >= 3 && this.result_a_4_5_6 <= 5) {
        this.result_a += 5
      } else if (this.result_a_4_5_6 >= 6 && this.result_a_4_5_6 <= 7) {
        this.result_a += 4
      } else if (this.result_a_4_5_6 >= 8 && this.result_a_4_5_6 <= 9) {
        this.result_a += 3
      } else if (this.result_a_4_5_6 >= 10 && this.result_a_4_5_6 <= 11) {
        this.result_a += 2
      } else if (this.result_a_4_5_6 === 12) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion4か5か6がクリック出来てません！')
      }

      this.result_a_7 = 5 - Number(this.question_a_7)
      if (this.result_a_7 === 1) {
        this.result_a += 4
      } else if (this.result_a_7 === 2) {
        this.result_a += 3
      } else if (this.result_a_7 === 3) {
        this.result_a += 2
      } else if (this.result_a_7 === 4) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion7がクリック出来てません！')
      }

      this.result_a_12_13_14 = (10 - (Number(this.question_a_12) + Number(this.question_a_13))) + Number(this.question_a_14)
      if (this.result_a_12_13_14 === 3) {
        this.result_a += 5
      } else if (this.result_a_12_13_14 >= 4 && this.result_a_12_13_14 <= 5) {
        this.result_a += 4
      } else if (this.result_a_12_13_14 >= 6 && this.result_a_12_13_14 <= 7) {
        this.result_a += 3
      } else if (this.result_a_12_13_14 >= 8 && this.result_a_12_13_14 <= 9) {
        this.result_a += 2
      } else if (this.result_a_12_13_14 >= 10 && this.result_a_12_13_14 <= 12)  {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion12か13か14がクリック出来てません！')
      }

      this.result_a_15 = 5 - Number(this.question_a_15)
      if (this.result_a_15 === 1) {
        this.result_a += 4
      } else if (this.result_a_15 === 2) {
        this.result_a += 3
      } else if (this.result_a_15 === 3) {
        this.result_a += 2
      } else if (this.result_a_15 === 4) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion15がクリック出来てません！')
      }

      this.result_a_8_9_10 = 15 - (Number(this.question_a_8) + Number(this.question_a_9) + Number(this.question_a_10))
      if (this.result_a_8_9_10 >= 11 && this.result_a_8_9_10 <= 12) {
        this.result_a += 5
      } else if (this.result_a_8_9_10 >= 9 && this.result_a_8_9_10 <= 10) {
        this.result_a += 4
      } else if (this.result_a_8_9_10 >=7 && this.result_a_8_9_10 <= 8) {
        this.result_a += 3
      } else if (this.result_a_8_9_10 >=5 && this.result_a_8_9_10 <= 6) {
        this.result_a += 2
      } else if (this.result_a_8_9_10 >= 3 && this.result_a_8_9_10 <= 4) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion8か9か10がクリック出来てません！')
      }

      this.result_a_11 = Number(this.question_a_11)
      if (this.result_a_11 === 4) {
        this.result_a += 4
      } else if (this.result_a_11 === 3) {
        this.result_a += 3
      } else if (this.result_a_11 === 2) {
        this.result_a += 2
      } else if (this.result_a_11 === 1) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion11がクリック出来てません！')
      }

      this.result_a_16 = 5 - Number(this.question_a_16)
      if (this.result_a_16 === 4) {
        this.result_a += 5
      } else if (this.result_a_16 === 3) {
        this.result_a += 3
      } else if (this.result_a_16 === 2) {
        this.result_a += 2
      } else if (this.result_a_16 === 1) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion16がクリック出来てません！')
      }

      this.result_a_17 = 5 - Number(this.question_a_17)
      if (this.result_a_17 === 4) {
        this.result_a += 5
      } else if (this.result_a_17 === 3) {
        this.result_a += 3
      } else if (this.result_a_17 === 2) {
        this.result_a += 2
      } else if (this.result_a_17 === 1) {
        this.result_a += 1
      } else {
        alert('1ページ目のquestion17がクリック出来てません！')
      }

      // ここからB
      // ここからB
      // ここからB

      this.result_b_1_2_3 = (Number(this.question_b_1) + Number(this.question_b_2) + Number(this.question_b_3))
      if (this.result_b_1_2_3 >= 10 && this.result_b_1_2_3 <= 12) {
        this.result_b += 5
      } else if (this.result_b_1_2_3 >= 8 && this.result_b_1_2_3 <= 9) {
        this.result_b += 4
      } else if (this.result_b_1_2_3 >= 6 && this.result_b_1_2_3 <= 7) {
        this.result_b += 3
      } else if (this.result_b_1_2_3 >= 4 && this.result_b_1_2_3 <= 5) {
        this.result_b += 2
      } else if (this.result_b_1_2_3 === 3)  {
        this.result_b += 1
      } else {
        alert('2ページ目のquestion1か2か3がクリック出来てません！')
      }

      this.result_b_4_5_6 = (Number(this.question_b_4) + Number(this.question_b_5) + Number(this.question_b_6))
      if (this.result_b_4_5_6 === 3) {
        this.result_b += 5
      } else if (this.result_b_4_5_6 >= 4 && this.result_b_4_5_6 <= 5) {
        this.result_b += 4
      } else if (this.result_b_4_5_6 >= 6 && this.result_b_4_5_6 <= 7) {
        this.result_b += 3
      } else if (this.result_b_4_5_6 >= 8 && this.result_b_4_5_6 <= 9) {
        this.result_b += 2
      } else if (this.result_b_4_5_6 >= 10 && this.result_b_4_5_6 <= 12)  {
        this.result_b += 1
      } else {
        alert('2ページ目のquestion4か5か6がクリック出来てません！')
      }

      this.result_b_7_8_9 = (Number(this.question_b_7) + Number(this.question_b_8) + Number(this.question_b_9))
      if (this.result_b_7_8_9 === 3) {
        this.result_b += 5
      } else if (this.result_b_7_8_9 === 4) {
        this.result_b += 4
      } else if (this.result_b_7_8_9 >= 5 && this.result_b_7_8_9 <= 7) {
        this.result_b += 3
      } else if (this.result_b_7_8_9 >= 8 && this.result_b_7_8_9 <= 10) {
        this.result_b += 2
      } else if (this.result_b_7_8_9 >= 11 && this.result_b_7_8_9 <= 12)  {
        this.result_b += 1
      } else {
        alert('2ページ目のquestion4か5か6がクリック出来てません！')
      }

      this.result_b_10_11_12 = (Number(this.question_b_10) + Number(this.question_b_11) + Number(this.question_b_12))
      if (this.result_b_10_11_12 === 3) {
        this.result_b += 5
      } else if (this.result_b_10_11_12 === 4) {
        this.result_b += 4
      } else if (this.result_b_10_11_12 >= 5 && this.result_b_10_11_12 <= 7) {
        this.result_b += 3
      } else if (this.result_b_10_11_12 >= 8 && this.result_b_10_11_12 <= 9) {
        this.result_b += 2
      } else if (this.result_b_10_11_12 >= 10 && this.result_b_10_11_12 <= 12)  {
        this.result_b += 1
      } else {
        alert('2ページ目のquestion10か11か12がクリック出来てません！')
      }

      this.result_b_13_14_15_16_17_18 = (Number(this.question_b_13) + Number(this.question_b_14)+ Number(this.question_b_15)
      + Number(this.question_b_16) + Number(this.question_b_17) + Number(this.question_b_18))
      if (this.result_b_13_14_15_16_17_18 === 6) {
        this.result_b += 5
      } else if (this.result_b_13_14_15_16_17_18 >= 7 && this.result_b_13_14_15_16_17_18 <= 8) {
        this.result_b += 4
      } else if (this.result_b_13_14_15_16_17_18 >= 9 && this.result_b_13_14_15_16_17_18 <= 12) {
        this.result_b += 3
      } else if (this.result_b_13_14_15_16_17_18 >= 13 && this.result_b_13_14_15_16_17_18 <= 16) {
        this.result_b += 2
      } else if (this.result_b_13_14_15_16_17_18 >= 17 && this.result_b_13_14_15_16_17_18 <= 24)  {
        this.result_b += 1
      } else {
        alert('2ページ目のquestion13か14か15か16か17か18がクリック出来てません！')
      }

      this.result_b_19_20_21_22_23_24_25_26_27_28_29 = (Number(this.question_b_19) + Number(this.question_b_20)+ Number(this.question_b_21)
      + Number(this.question_b_22) + Number(this.question_b_23) + Number(this.question_b_24) + Number(this.question_b_25) + Number(this.question_b_24)
      + Number(this.question_b_25) + Number(this.question_b_26) + Number(this.question_b_27) + Number(this.question_b_28) + Number(this.question_b_29))
      if (this.result_b_19_20_21_22_23_24_25_26_27_28_29 === 11) {
        this.result_b += 5
      } else if (this.result_b_19_20_21_22_23_24_25_26_27_28_29 >= 12 && this.result_b_19_20_21_22_23_24_25_26_27_28_29 <= 15) {
        this.result_b += 4
      } else if (this.result_b_19_20_21_22_23_24_25_26_27_28_29 >= 16 && this.result_b_19_20_21_22_23_24_25_26_27_28_29 <= 21) {
        this.result_b += 3
      } else if (this.result_b_19_20_21_22_23_24_25_26_27_28_29 >= 22 && this.result_b_19_20_21_22_23_24_25_26_27_28_29 <= 26) {
        this.result_b += 2
      } else if (this.result_b_19_20_21_22_23_24_25_26_27_28_29 >= 27 && this.result_b_19_20_21_22_23_24_25_26_27_28_29 <= 44)  {
        this.result_b += 1
      } else {
        alert('2ページ目のquestion19か20か21か22か23か24か25か26か27か28か29がクリック出来てません！')
      }

      // ここからC
      // ここからC
      // ここからC

      this.result_c_1_4_7 = 15 - (Number(this.question_c_1) + Number(this.question_c_4) + Number(this.question_c_7))
      if (this.result_c_1_4_7 >= 11 && this.result_c_1_4_7 <= 12) {
        this.result_c += 5
      } else if (this.result_c_1_4_7 >= 9 && this.result_c_1_4_7 <= 10) {
        this.result_c += 4
      } else if (this.result_c_1_4_7 >= 7 && this.result_c_1_4_7 <= 8) {
        this.result_c += 3
      } else if (this.result_c_1_4_7 >= 5 && this.result_c_1_4_7 <= 6) {
        this.result_c += 2
      } else if (this.result_c_1_4_7 >= 3 && this.result_c_1_4_7 <= 4) {
        this.result_c += 1
      } else {
        alert('3ページ目のquestion1か4か7がクリック出来てません！')
      }

      this.result_c_2_5_8 = 15 - (Number(this.question_c_2) + Number(this.question_c_5) + Number(this.question_c_8))
      if (this.result_c_2_5_8 === 12) {
        this.result_c += 5
      } else if (this.result_c_2_5_8 >= 10 && this.result_c_2_5_8 <= 11) {
        this.result_c += 4
      } else if (this.result_c_2_5_8 >= 8 && this.result_c_2_5_8 <= 9) {
        this.result_c += 3
      } else if (this.result_c_2_5_8 >= 6 && this.result_c_2_5_8 <= 7) {
        this.result_c += 2
      } else if (this.result_c_2_5_8 >= 3 && this.result_c_2_5_8 <= 5) {
        this.result_c += 1
      } else {
        alert('3ページ目のquestion2か5か8がクリック出来てません！')
      }

      this.result_c_3_6_9 = 15 - (Number(this.question_c_3) + Number(this.question_c_6) + Number(this.question_c_9))
      if (this.result_c_3_6_9 === 12) {
        this.result_c += 5
      } else if (this.result_c_3_6_9 >= 10 && this.result_c_3_6_9 <= 11) {
        this.result_c += 4
      } else if (this.result_c_3_6_9 === 9) {
        this.result_c += 3
      } else if (this.result_c_3_6_9 >= 7 && this.result_c_3_6_9 <= 8) {
        this.result_c += 2
      } else if (this.result_c_3_6_9 >= 3 && this.result_c_3_6_9 <= 6) {
        this.result_c += 1
      } else {
        alert('3ページ目のquestion3か6か9がクリック出来てません！')
      }




      //ここから計算結果
      if (this.result_b <= 12) {
        this.totalText = '高ストレス'
      } else if (this.result_b <= 17 && this.result_a + this.result_c <= 26)  {
        this.totalText = '高ストレス'
      } else {
        this.totalText = '正常'
      }

      // 結果表示画面
      this.page += 1

      // 再度計算すると前の結果から足してしまうので、最後に0にする。
      this.result_a = 0
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
