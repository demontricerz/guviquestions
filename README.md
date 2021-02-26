> ## VQ1 Mancunian and fantabulous pairs

**Problem Statement**
Mancunian challenges you to solve the following problem. Given an array, find the total number of  **distinct**  fantabulous pairs over all its subarrays.

**Explanation**
- First off, some definitions.  
- An array of length at least 2 having distinct integers is said to be fantabulous iff the second highest element lies  **strictly to the left**  of the highest value. 
- For example,  _[1, 2, 13, 10, 15]_  is fantabulous as the second-highest value  _13_  lies to the left of highest value  _15_.  
- For every fantabulous array, we define a fantabulous pair  **(a, b)**  where  **a**  denotes the index of the second-highest value (1-indexed) and  **b**  denotes the index of the highest value (1-indexed). 
- In the above array, the fantabulous pair is (3, 5).  

**Input Description**  

    The first line contains an integer  **N**  denoting the length of the array. 
    The next line contains  **N**  **distinct**  integers denoting the elements of the array.

**Output Description**  

    Output a single integer which is the answer to the problem.

**Constraints:**  

    1 <= N <= 106  
    1 <= array elements <= 109  
    Array elements are distinct.

**Time Limit:**

    Time Limit: 2000

**Sample Input**

    4
	1 3 2 4

**Sample Output**

    3

**Test Case 1**

**Input**

    500
	499 42 497 175 266 414 481 315 246 277 108 288 435 430 386 124 278 91 201 32 34 11 206 252 493 81 157 325 300 340 170 104 331 46 249 280 90 190 192 443 113 240 100 208 248 180 148 57 334 466 225 461 222 78 366 467 178 244 322 498 6 31 151 447 352 383 199 354 465 197 337 212 7 92 423 59 382 367 455 19 355 184 130 255 376 431 194 305 16 132 387 51 349 58 294 438 155 378 56 270 43 102 258 23 105 460 500 399 394 469 181 238 231 21 223 10 391 80 301 159 402 451 363 262 472 449 247 384 15 241 214 141 177 429 365 61 4 347 154 426 226 267 167 419 256 264 125 415 261 133 398 284 303 137 478 54 203 1 313 309 109 285 369 107 84 297 188 257 202 185 358 275 474 360 83 348 396 319 237 412 152 163 150 60 485 370 312 166 20 274 71 345 442 205 198 259 18 24 147 234 70 421 373 41 2 79 480 393 179 324 12 424 411 456 193 462 388 295 95 403 38 464 9 87 119 33 400 341 228 422 14 489 164 488 450 311 162 292 459 144 385 404 282 458 169 323 330 380 114 291 321 168 122 490 428 85 98 296 436 487 17 452 254 293 140 106 471 332 36 314 407 326 290 211 364 448 74 401 486 135 306 397 351 116 123 149 94 156 44 310 66 446 146 235 317 236 439 216 316 417 52 86 73 110 118 153 245 496 441 195 232 62 30 308 374 359 483 5 368 37 138 218 161 196 395 25 390 271 272 299 353 35 408 88 215 253 242 8 48 495 379 392 344 28 63 136 454 329 333 263 53 318 335 142 362 286 145 64 227 494 457 39 406 186 115 97 111 82 101 69 491 328 477 484 204 320 420 287 26 65 307 207 209 165 139 418 76 182 183 158 45 239 121 189 99 381 126 269 427 217 336 389 174 463 72 29 413 281 356 75 160 425 143 273 377 405 492 375 298 453 468 191 129 361 346 112 437 210 128 127 96 289 229 230 279 103 473 432 89 445 200 172 357 176 13 93 339 55 67 265 213 342 268 68 410 220 47 3 409 27 479 49 50 219 243 440 77 40 304 131 302 171 433 482 221 187 371 251 117 338 416 476 276 350 233 327 283 260 372 120 470 173 444 250 22 224 434 475 134 343

**Output**

    820
