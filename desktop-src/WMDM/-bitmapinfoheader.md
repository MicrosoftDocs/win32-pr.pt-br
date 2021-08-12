---
title: Estrutura de _BITMAPINFOHEADER
description: A \_ estrutura BITMAPINFOHEADER define o formato de um quadro de vídeo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Estrutura de _BITMAPINFOHEADER Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2d0da3d05fe050f32d5a35bbbe7de558e1c4962fa84a958855b2960e343942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586880"
---
# <a name="_bitmapinfoheader-structure"></a>\_Estrutura BITMAPINFOHEADER

A estrutura **\_ BITMAPINFOHEADER** define o formato de um quadro de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**bidimensional**
</dt> <dd>

Especifica o número de bytes exigidos pela estrutura.

</dd> <dt>

**bilargura**
</dt> <dd>

Especifica a largura do bitmap, em pixels.

</dd> <dt>

**biHeight**
</dt> <dd>

Especifica a altura do bitmap, em pixels. Se a **interheight** for positiva, o bitmap será um DIB de baixo para cima e sua origem será o canto inferior esquerdo. Se a **interheight** for negativa, o bitmap será um DIB de cima para baixo e sua origem será o canto superior esquerdo. Se a **interheight** for negativa, indicando um DIB de cima para baixo, a **biCompression** deverá ser bi \_ RGB ou bi \_ BITFIELDS. Os DIBs de cima para baixo não podem ser compactados.

</dd> <dt>

**monoplans**
</dt> <dd>

Especifica o número de planos para o dispositivo de destino. Esse valor deve ser definido como 1.

</dd> <dt>

**biBitCount**
</dt> <dd>

Especifica o número de bits por pixel. O membro **biBitCount** da estrutura **BITMAPINFOHEADER** determina o número de bits que definem cada pixel e o número máximo de cores no bitmap. Esse membro deve ser um dos valores a seguir.



| Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | O bitmap é monocromático e o membro bmiColors contém duas entradas. Cada bit na matriz de bitmap representa um pixel. Se o bit estiver claro, o pixel será exibido com a cor da primeira entrada na tabela bmiColors; Se o bit for definido, o pixel terá a cor da segunda entrada na tabela.                                                                                                                                                                                                                                                                                                        |
| 2     | O bitmap tem quatro valores de cor possíveis.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | O bitmap tem um máximo de 16 cores e o membro bmiColors contém até 16 entradas. Cada pixel no bitmap é representado por um índice de 4 bits na tabela de cores. Por exemplo, se o primeiro byte no bitmap for 0x1F, o byte representará dois pixels. O primeiro pixel contém a cor na segunda entrada de tabela e o segundo pixel contém a cor na décima primeira entrada da tabela.                                                                                                                                                                                                                 |
| 8     | O bitmap tem um máximo de 256 cores e o membro bmiColors contém até 256 entradas. Nesse caso, cada byte na matriz representa um único pixel.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | O bitmap tem um máximo de 2 ^ 16 cores. Se o membro de bicompressão do BITMAPINFOHEADER for BI \_ RGB, o membro bmiColors será **nulo**. Cada palavra na matriz de bitmap representa um único pixel. As intensidades relativas de vermelho, verde e azul são representadas com 5 bits para cada componente de cor. O valor de Blue é, no mínimo, 5 bits, seguido de 5 bits cada para verde e vermelho. O bit mais significativo não é usado. A tabela de cores bmiColors é usada para otimizar as cores usadas em dispositivos baseados em paleta e deve conter o número de entradas especificado pelo membro biClrUsed. |
| 24    | O bitmap tem um máximo de 2 ^ 24 cores e o membro bmiColors é **nulo**. Cada terceto de 3 bytes na matriz de bitmap representa as intensidades relativas de azul, verde e vermelho, respectivamente, para um pixel. A tabela de cores bmiColors é usada para otimizar as cores usadas em dispositivos baseados em paleta e deve conter o número de entradas especificado pelo membro biClrUsed.                                                                                                                                                                                                                                     |
| 32    | O bitmap tem um máximo de 2 ^ 32 cores. Se o membro de bicompressão for BI \_ RGB, o membro bmiColors será **nulo**. Cada DWORD na matriz de bitmap representa as intensidades relativas de azul, verde e vermelho, respectivamente, para um pixel. O byte alto em cada DWORD não é usado. A tabela de cores bmiColors é usada para otimizar as cores usadas em dispositivos baseados em paleta e deve conter o número de entradas especificado pelo membro biClrUsed.                                                                                                                                                                 |



 

</dd> <dt>

**bicompressão**
</dt> <dd>

Especifica o tipo de compactação para um bitmap de parte inferior compactado (o DIBs superior não pode ser compactado). Esse membro pode ser um dos valores a seguir.



| Valor         | Descrição                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RGB de BI \_       | Um formato descompactado.                                                                                                                                                                                                                                                                                            |
| \_BITFIELDS bi | Especifica que o bitmap não é compactado e que a tabela de cores consiste em três máscaras de cor DWORD que especificam os componentes vermelho, verde e azul, respectivamente, de cada pixel. Isso é válido quando usado com bitmaps de 16-BPP e 32-bpp. esse valor é válido no Microsoft Windows CE versão 2,0 e posterior. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Especifica o tamanho da imagem, em bytes. Isso pode ser definido como zero para \_ bitmaps RGB de BI.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Especifica a resolução horizontal, em pixels por medidor, do dispositivo de destino para o bitmap. Um aplicativo pode usar esse valor para selecionar um bitmap de um grupo de recursos que melhor corresponda às características do dispositivo atual.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Especifica a resolução vertical, em pixels por medidor, do dispositivo de destino para o bitmap.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Especifica o número de índices de cores na tabela de cores que são realmente usados pelo bitmap. Se esse valor for zero, o bitmap usará o número máximo de cores correspondentes ao valor do membro **biBitCount** para o modo de compactação especificado pela **biCompression**.

</dd> <dt>

**biClrImportant**
</dt> <dd>

Especifica o número de índices de cores necessários para exibir o bitmap. Se esse valor for zero, todas as cores serão necessárias.

Se biClrUsed for diferente de zero e o membro biBitCount for menor que 16, o membro biClrUsed especificará o número real de cores que o mecanismo de gráficos ou o driver de dispositivo acessa. Se biBitCount for 16 ou superior, o membro biClrUsed especificará o tamanho da tabela de cores usada para otimizar o desempenho das paletas de cores do sistema. Se biBitCount for igual a 16 ou 32, a paleta de cores ideal começará imediatamente após as três máscaras DWORD.

Se o bitmap é um bitmap empacotado (um bitmap no qual a matriz de bitmap segue imediatamente a \_ estrutura BITMAPINFOHEADER e é referenciada por um único ponteiro), o membro biClrUsed deve ser zero ou o tamanho real da tabela de cores.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura está contida em uma estrutura **\_ VIDEOINFOHEADER** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





