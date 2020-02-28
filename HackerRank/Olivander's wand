/*https://www.hackerrank.com/challenges/harry-potter-and-wands/problem?h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen*/

SELECT W.ID, WP.AGE, W.COINS_NEEDED, W.POWER
FROM WANDS W 
JOIN WANDS_PROPERTY WP
ON W.CODE = WP.CODE
WHERE W.COINS_NEEDED = 
  (SELECT MIN(W1.COINS_NEEDED)
   FROM WANDS W1
   JOIN WANDS_PROPERTY WP1
   ON W1.CODE = WP1.CODE
   WHERE WP1.IS_EVIL = 0 
   AND W.POWER = W1.POWER
   AND WP.AGE = WP1.AGE)
ORDER BY W.POWER DESC, WP.AGE DESC;
