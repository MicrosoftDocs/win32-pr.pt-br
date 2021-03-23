---
title: Usando progressos para expressar o layout de enchimento e de memória
description: Os dezenases de DirectML são descritos pelas propriedades conhecidas como os *tamanhos* e os *avanços* do tensor.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548248"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a>Usando progressos para expressar o layout de enchimento e de memória

Os tempos &mdash; de DirectML que são apoiados por buffers do Direct3D 12 &mdash; são descritos pelas propriedades conhecidas como os *tamanhos* e os *avanços* do tensor. Os *tamanhos* de tensor descrevem as dimensões lógicas do tensor. Por exemplo, um tensor 2D pode ter uma altura de 2 e uma largura de 3. Logicamente, o tensor tem 6 elementos distintos, embora os tamanhos não especifiquem como esses elementos são armazenados na memória. Os *passos* do tensor descrevem o layout da memória física dos elementos do tensor.

## <a name="two-dimensional-2d-arrays"></a>Matrizes bidimensionais (2D)

Considere um tensor 2D com altura de 2 e uma largura de 3; os dados incluem caracteres textuais. No C/C++, isso pode ser expresso usando uma matriz multidimensional.

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

A exibição lógica do tensor acima é visualizada abaixo.

```console
A B C
D E F
```

No C/C++, uma matriz multidimensional é armazenada em ordem de linha principal. Em outras palavras, os elementos consecutivos ao longo da dimensão de largura são armazenados de forma contígua no espaço de memória linear.

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Valor:|A|B|C|D|E|F

O *Stride* de uma dimensão é o número de elementos a serem ignorados para acessar o próximo elemento nessa dimensão. Os avanços expressam o layout do tensor na memória. Com uma ordem de linha principal, o stride da dimensão de largura é sempre 1, pois elementos adjacentes ao longo da dimensão são armazenados de forma contígua. O stride da dimensão de altura depende do tamanho da dimensão de largura; no exemplo acima, a distância entre elementos consecutivos ao longo da dimensão de altura (por exemplo, a a D) é igual à largura do tensor (que é 3 neste exemplo).

Para ilustrar um layout diferente, considere a ordem de coluna principal. Em outras palavras, os elementos consecutivos ao longo da dimensão de altura são armazenados de forma contígua no espaço de memória linear. Nesse caso, o stride de altura é sempre 1 e o stride de largura é 2 (o tamanho da dimensão de altura).

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Valor:|A|D|B|E|C|F

## <a name="higher-dimensions"></a>Dimensões mais altas

Quando se trata de mais de duas dimensões, é difícil fazer referência a um layout como linha-principal ou coluna-principal. Assim, o restante deste tópico usa termos e rótulos como esses.

- 2D: &mdash; a altura de "HW" é a dimensão de ordem mais alta (linha-principal).
- 2D: a largura "qu" &mdash; é a dimensão de ordem mais alta (coluna-principal).
- 3D: a profundidade de "DHW" &mdash; é a dimensão de ordem mais alta, seguida por Height e, em seguida, Width.
- 3D: a largura "WHD" &mdash; é a dimensão de ordem mais alta, seguida por altura e, em seguida, profundidade.
- 4D: "NCHW" &mdash; o número de imagens (tamanho do lote), em seguida, o número de canais, a altura e a largura.

Em geral, o stride *embalado* de uma dimensão é igual ao produto dos tamanhos das dimensões de ordem inferior. Por exemplo, com um layout "DHW", o D-Stride é igual a H * W; o H-Stride é igual a W; e o W-Stride é igual a 1. Os passos devem ser *empacotados* quando o tamanho físico total do tensor for igual ao tamanho lógico total do tensor; em outras palavras, não há nenhum espaço extra nem sobreposição de elementos.

Vamos estender o exemplo de 2D para três dimensões, para que tenhamos um tensor com profundidade 2, altura 2 e largura 3 (para um total de 12 elementos lógicos).

```console
A B C
D E F

G H I
J K L
```

Com um layout "DHW", esse tensor é armazenado da seguinte maneira.

Offset:|0|1|2|3|4|5|6|7|8|9|10|11|
-|-|-|-|-|-|-|-|-|-|-|-|-|
Valor:|A|B|C|D|E|F|G|H|I|J|K|L|

- D-Stride = altura (2) * largura (3) = 6 (por exemplo, a distância entre ' A ' e ' G ').
- H-Stride = largura (3) = 3 (por exemplo, a distância entre ' A ' e ' d').
- W-Stride = 1 (por exemplo, a distância entre ' A ' e ' B ').

O produto de ponto dos índices/coordenadas de um elemento e os avanços fornecem o deslocamento para esse elemento no buffer. Por exemplo, o deslocamento do elemento H (d = 1, H = 0, w = 1) é 7.

{1, 0, 1} ⋅ {6, 3, 1} = 1 * 6 + 0 * 3 + 1 * 1 = 7

## <a name="packed-tensors"></a>Dezenases em pacotes

Os exemplos acima ilustram os tempos de *empacotamento* . Um tensor é considerado *embalado* quando o tamanho lógico do tensor (em elementos) é igual ao tamanho físico do buffer (em elementos) e cada elemento tem um endereço/deslocamento exclusivo. Por exemplo, um 2x2x3 tensor será empacotado se o buffer tiver 12 elementos de comprimento e nenhum par de elementos compartilhar o mesmo deslocamento no buffer. Os dezenases incluídos são o caso mais comum; Mas os avanços permitem layouts de memória mais complexos.

## <a name="broadcasting-with-strides"></a>Transmitindo com progressos

Se o tamanho do buffer de um tensor (em elementos) for menor do que o produto de suas dimensões lógicas, então, será necessário haver alguma sobreposição de elementos. O caso usual para isso é conhecido como *transmissão*; onde os elementos de uma dimensão são uma duplicata de outra dimensão. Por exemplo, Vamos revisitar o exemplo de 2D. Digamos que desejamos um tensor que seja logicamente 2x3, mas a segunda linha é idêntica à primeira linha. Esta é a aparência.

```console
A B C
A B C
```

Isso pode ser armazenado como um tensor de HW/linha-principal empacotado. Mas um armazenamento mais compacto conterá apenas três elementos (A, B e C) e usará um stride de altura de 0 em vez de 3. Nesse caso, o tamanho físico do tensor é de três elementos, mas o tamanho lógico é de 6 elementos.

Em geral, se o stride de uma dimensão for 0, todos os elementos nas dimensões de ordem inferior serão repetidos ao longo da dimensão transmitida; por exemplo, se tensor for NCHW e o C-stride for 0, cada canal terá os mesmos valores ao longo de H e W.

## <a name="padding-with-strides"></a>Preenchimento com progressos

Um tensor será *preenchido* se seu tamanho físico for maior do que o tamanho mínimo necessário para ajustar seus elementos. Quando não há nenhum elemento de difusão nem sobreposição, o tamanho mínimo do tensor (em elementos) é simplesmente o produto de suas dimensões. Você pode usar a função auxiliar `DMLCalcBufferTensorSize` (consulte [funções auxiliares DirectML](dml-helper-functions.md) para obter uma listagem dessa função) para calcular o tamanho *mínimo* do buffer para seus DirectMLs.

Digamos que um buffer contenha os valores a seguir (os elementos ' x ' indicam valores de preenchimento).

0|1|2|3|4|5|6|7|8|9|
-|-|-|-|-|-|-|-|-|-|
A|B|C|x|x|D|E|F|x|x

O tensor preenchido pode ser descrito usando um stride de altura de 5 em vez de 3. Em vez de passar por três elementos para chegar à próxima linha, a etapa é de 5 elementos (três elementos *reais* mais 2 elementos de preenchimento). O preenchimento é comum em gráficos de computador, por exemplo, para garantir que uma imagem tenha um alinhamento de potência de dois.

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a>Descrições de tensor do buffer DirectML

O DirectML pode trabalhar com uma variedade de layouts de tensor físicos, já que a estrutura de [ **DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) tem ambos os `Sizes` `Strides` Membros e. Algumas implementações de operador podem ser mais eficientes com um layout específico, portanto, não é incomum alterar como os dados de tensor são armazenados para melhorar o desempenho.

A maioria dos operadores de DirectML requer 4D ou 5D, e a ordem dos valores de tamanhos e de progressos é fixa. Ao corrigir a ordem dos tamanhos e valores de Stride em uma descrição de tensor, é possível que DirectML inferir layouts físicos diferentes.

**4D**
- [**DML_BUFFER_TENSOR_DESC:: tamanhos**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-tamanho, C-tamanho, H-tamanho, W-size}
- [**DML_BUFFER_TENSOR_DESC:: prerides**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-Stride, C-Stride, H-Stride, W-Stride}

**5D**
- **DML_BUFFER_TENSOR_DESC:: tamanhos** = {N-tamanho, C-tamanho, D-tamanho, H-tamanho, W-tamanho}
- **DML_BUFFER_TENSOR_DESC:: prerides** = {N-Stride, C-Stride, D-Stride, H-Stride, W-Stride}

Se um operador DirectML exigir um 4D ou um tensor de 5D, mas os dados reais tiverem uma classificação menor (por exemplo, 2D), as dimensões principais deverão ser preenchidas com 1s. Por exemplo, um tensor de "HW" é definido usando **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, H, W}.

Se os dados do tensor forem armazenados em NCHW/NCDHW, não será necessário definir **DML_BUFFER_TENSOR_DESC:: Rides**, a menos que você queira difusão ou preenchimento. Você pode definir o campo de passos como `nullptr` . No entanto, se os dados de tensor forem armazenados em outro layout, como NHWC, você precisará de sobrerides para expressar a transformação de NCHW para esse layout.

Para obter um exemplo simples, considere a descrição de um tensor 2D com a altura 3 e a largura 5.

**NCHW empacotados (sobrerides implícitos)**
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: progressos** = `nullptr`

**NCHW empacotados (transrides explícitos)**
- N-Stride = C-tamanho * H-tamanho * W-tamanho = 1 * 3 * 5 = 15
- C-Stride = H-tamanho * W-tamanho = 3 * 5 = 15
- H-Stride = W-tamanho = 5
- W-Stride = 1
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: prerides** = {15, 15, 5, 1}

**NHWC empacotados**
- N-Stride = H-tamanho * W-tamanho * C-tamanho = 3 * 5 * 1 = 15
- H-Stride = W-tamanho * C-size = 5 * 1 = 5
- W-Stride = C-size = 1
- C-Stride = 1
- **DML_BUFFER_TENSOR_DESC:: sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: prerides** = {15, 1, 5, 1}

## <a name="see-also"></a>Confira também

* [Funções auxiliares DirectML](dml-helper-functions.md)
* [Estrutura de DML_BUFFER_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
