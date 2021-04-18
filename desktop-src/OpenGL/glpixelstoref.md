---
title: função glPixelStoref (GL. h)
description: Define os modos de armazenamento em pixels. | função glPixelStoref (GL. h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- função glPixelStoref OpenGL
topic_type:
- apiref
api_name:
- glPixelStoref
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc35613be68bb142b14a7e8278d6e0b89f05d78e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104569649"
---
# <a name="glpixelstoref-function"></a>função glPixelStoref

Define os modos de armazenamento em pixels.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* 
</dt> <dd>

O nome simbólico do parâmetro a ser definido. Seis dos parâmetros de armazenamento afetam o modo como os dados de pixel são retornados à memória do cliente e, portanto, são significativos apenas para comandos [**glReadPixels**](glreadpixels.md) . Elas são as seguintes:



| Parâmetro de armazenamento                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BYTES de permuta do GL \_ Pack \_ \_                                       | Se for true, a ordenação de bytes para componentes de cores multibyte, componentes de profundidade, índices de cores ou índices de estêncil será revertida. Ou seja, se um componente de quatro bytes for composto de bytes *b* 0, *b* 1, *b* 2, *b* 3, ele será armazenado na memória como *b* 3, *b* 2, *b* 1, *b* 0 se os bytes de permuta do GL \_ Pack \_ \_ forem verdadeiros. \_ \_ Os bytes de permuta do GL Pack \_ não têm nenhum efeito na ordem de memória dos componentes em um pixel, somente na ordem de bytes em componentes ou índices. Por exemplo, os três componentes de um pixel de formato do GL \_ RGB sempre são armazenados com vermelho primeiro, verde segundo e azul terceiro, independentemente do valor dos bytes de permuta do GL \_ Pack \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                               |
| LSB do GL \_ Pack \_ \_ primeiro                                        | Se for true, os bits serão ordenados em um byte do menos significativo para o mais significativo; caso contrário, o primeiro bit em cada byte é o mais significativo. Esse parâmetro é significativo apenas para dados de bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| comprimento da linha do GL \_ Pack \_ \_                                       | Se for maior que zero, \_ o \_ comprimento da linha do GL Pack \_ definirá o número de pixels em uma linha. Se o primeiro pixel de uma linha for colocado no local p na memória, o local do primeiro pixel da próxima linha será obtido ignorando ![ a equação mostrando o local do primeiro pixel da próxima linha no GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ \]componentes ou índices de nova linha, em que *n* é o número de componentes ou índices em um pixel, *l* é o número de pixels em uma linha (comprimento de linha do GL \- Pack \- \- se for maior que zero, o argumento de largura para a rotina de pixel de outra forma), *um* é o valor do alinhamento do \- pacote GL \- , e *s* é o tamanho, em bytes, de um único componente (se  <  *s*, é como se fosse *um*  =  *s*). no caso de valores de 1 bit, o local da próxima linha é obtido ignorando ![ a equação mostrando a localização da próxima linha no GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> componentes ou índices. O *componente* do Word nesta descrição refere-se aos valores não indexados em vermelho, verde, azul, alfa e profundidade. O formato de armazenamento GL \_ RGB, por exemplo, tem três componentes por pixel: primeiro vermelho, depois verde e, finalmente, azul.<br/> |
| O GL \_ Pack \_ ignora \_ pixels e <br/> o GL \_ Pack \_ ignora \_ linhas | Esses valores são fornecidos como uma conveniência para o programador; Eles não fornecem nenhuma funcionalidade que não pode ser duplicada simplesmente incrementando o ponteiro passado para [**glReadPixels**](glreadpixels.md). A definição do GL \_ Pack \_ Skip \_ pixels para *i* equivale a incrementar o ponteiro por *i n* componentes ou índices, em que *n* é o número de componentes ou índices em cada pixel. Definir \_ \_ \_ as linhas do GL Pack Skip para *j* é equivalente a incrementar o ponteiro por componentes ou índices *j k* , em que *k* é o número de componentes ou índices por linha, como calculado acima na \_ \_ seção comprimento de linha do GL Pack \_ .                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_alinhamento do pacote GL \_                                         | Especifica os requisitos de alinhamento para o início de cada linha de pixel na memória. Os valores permitidos são 1 (alinhamento de byte), 2 (linhas alinhadas a bytes pares), 4 (alinhamento de palavras) e 8 (linhas iniciam em limites de palavras duplas).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Os outros seis parâmetros de armazenamento afetam o modo como os dados de pixel são lidos da memória do cliente. Esses valores são significativos para [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)e [**glPolygonStipple**](glpolygonstipple.md). Elas são as seguintes:



| Parâmetro de armazenamento                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_bytes de permuta de descompactação GL \_ \_                                         | Se for true, a ordenação de bytes para componentes de cores multibyte, componentes de profundidade, índices de cores ou índices de estêncil será revertida. Ou seja, se um componente de quatro bytes for composto de bytes *b* 0, *b* 1, *b* 2, *b* 3, ele será armazenado na memória como *b* 3, *b* 2, *b* 1, *b* 0 se o GL \_ Unpack \_ swap \_ bytes for true. \_O GL Unpack \_ swap \_ bytes não tem nenhum efeito na ordem de memória dos componentes em um pixel, somente na ordem de bytes em componentes ou índices. Por exemplo, os três componentes de um pixel de formato do GL \_ RGB sempre são armazenados com vermelho primeiro, verde segundo e azul terceiro, independentemente do valor de \_ bytes de permuta de Unpack GL \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ Unpack \_ LSB \_ primeiro                                          | Se for true, os bits serão ordenados em um byte do menos significativo para o mais significativo; caso contrário, o primeiro bit em cada byte é o mais significativo. Isso é significativo apenas para dados de bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_comprimento de linha de descompactação GL \_ \_                                         | Se for maior que zero, o \_ comprimento de linha de descompactação GL \_ \_ definirá o número de pixels em uma linha. Se o primeiro pixel de uma linha for colocado no local p na memória, o local do primeiro pixel da próxima linha será obtido ignorando ![ a equação mostrando o local do primeiro pixel da próxima linha no GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ \]componentes ou índices de nova linha, em que *n* é o número de componentes ou índices em um pixel, *l* é o número de pixels em uma linha (comprimento de linha do GL \- Pack \- \- se for maior que zero, o argumento de largura para a rotina de pixel de outra forma), *um* é o valor do alinhamento do \- pacote GL \- , e *s* é o tamanho, em bytes, de um único componente (se  <  *s*, é como se fosse *um*  =  *s*). no caso de valores de 1 bit, o local da próxima linha é obtido ignorando ![ a equação mostrando a localização da próxima linha no GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> componentes ou índices. O *componente* do Word nesta descrição refere-se aos valores não indexados em vermelho, verde, azul, alfa e profundidade. O formato de armazenamento GL \_ RGB, por exemplo, tem três componentes por pixel: primeiro vermelho, depois verde e, finalmente, azul.<br/> |
| GL \_ desembalar \_ ignorar \_ pixels e <br/> o GL \_ desembalar \_ ignora \_ linhas | Esses valores são fornecidos como uma conveniência para o programador; Eles não fornecem nenhuma funcionalidade que não pode ser duplicada simplesmente incrementando o ponteiro passado para [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)ou [**glPolygonStipple**](glpolygonstipple.md). Definir \_ o Unpack GL \_ ignora \_ pixels para *i* é equivalente a incrementar o ponteiro por *i n* componentes ou índices, em que *n* é o número de componentes ou índices em cada pixel. Definir \_ as linhas do GL Unpack \_ Skip \_ para *j* é equivalente a incrementar o ponteiro por componentes ou índices *j k* , em que *k* é o número de componentes ou índices por linha, como calculado acima \_ na \_ seção tamanho da linha gl Unpack \_ .                                                                                                                                                                                                                                    |
| \_alinhamento de descompactação GL \_                                           | Especifica os requisitos de alinhamento para o início de cada linha de pixel na memória. Os valores permitidos são 1 (alinhamento de byte), 2 (linhas alinhadas a bytes pares), 4 (alinhamento de palavras) e 8 (linhas iniciam em limites de palavras duplas).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

O valor para o qual *pname* é definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glPixelStore** define os modos de armazenamento em pixel que afetam a operação de [**glDrawPixels**](gldrawpixels.md) e [**glReadPixels**](glreadpixels.md) subsequentes, bem como o desempacotamento de padrões de polígono Stipple (consulte [**GlPolygonStipple**](glpolygonstipple.md)), bitmaps (consulte [**glBitmap**](glbitmap.md)) e padrões de textura (consulte [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md)).

A tabela a seguir fornece o tipo, o valor inicial e o intervalo de valores válidos para cada um dos parâmetros de armazenamento que podem ser definidos com **glPixelStore**.



| Pname                    | Tipo    | Valor inicial | Intervalo Válido   |
|--------------------------|---------|---------------|---------------|
| BYTES de permuta do GL \_ Pack \_ \_    | Boolean | false         | true ou false |
| BYTES de permuta do GL \_ Pack \_ \_    | Boolean | false         | true ou false |
| comprimento da linha do GL \_ Pack \_ \_    | integer | 0             | \[0,?)        |
| o GL \_ Pack \_ ignora \_ linhas     | integer | 0             | \[0,?)        |
| o GL \_ Pack \_ ignora \_ pixels   | integer | 0             | \[0,?)        |
| \_alinhamento do pacote GL \_      | Número inteiro | 4             | 1, 2, 4 ou 8 |
| \_bytes de permuta de descompactação GL \_ \_  | Boolean | false         | true ou false |
| GL \_ Unpack \_ LSB \_ primeiro   | Boolean | false         | true ou false |
| \_comprimento de linha de descompactação GL \_ \_  | integer | 0             | \[0,?)        |
| o GL \_ desembalar \_ ignora \_ linhas   | integer | 0             | \[0,?)        |
| o GL \_ desembalar \_ ignorar \_ pixels | integer | 0             | \[0,?)        |
| \_alinhamento de descompactação GL \_    | Número inteiro | 4             | 1, 2, 4 ou 8 |



 

A função **glPixelStoref** pode ser usada para definir qualquer parâmetro de armazenamento de pixel. Se o tipo de parâmetro for booliano e se *param* for 0,0, o parâmetro será false; caso contrário, ele será definido como true. Se *pname* for um parâmetro de tipo inteiro, *param* será arredondado para o número inteiro mais próximo.

Da mesma forma, a função **glPixelStorei** também pode ser usada para definir qualquer um dos parâmetros de armazenamento de pixel. Os parâmetros boolianos são definidos como false se *param* for 0 e true caso contrário. O parâmetro *param* é convertido em ponto flutuante antes de ser atribuído a parâmetros de valor real.

Os modos de armazenamento de pixel em vigor quando [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glBitmap**](glbitmap.md)ou [**glPolygonStipple**](glpolygonstipple.md) são colocados em uma lista de exibição controlam a interpretação de dados de memória. Os modos de armazenamento de pixel em vigor quando uma lista de exibição é executada não são significativos.

As funções a seguir recuperam informações relacionadas ao **glPixelStore**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumentos de permuta do argumento GL \_ Pack \_ \_

**glGet** com Argument GL \_ Pack \_ LSB \_ primeiro

**glGet** com o comprimento de linha do argumento GL \_ Pack \_ \_

**glGet** com o argumento GL \_ Pack \_ ignora \_ linhas

**glGet** com o argumento GL \_ Pack \_ Skip \_ pixels

**glGet** com alinhamento do argumento GL \_ Pack \_

**glGet** com Argument GL \_ Unpack \_ swap \_ bytes

**glGet** com Argument GL \_ Unpack \_ LSB \_ First

**glGet** com o \_ comprimento de linha de descompactação do argumento GL \_ \_

**glGet** com argumento GL \_ descompactar \_ \_ linhas Skip

**glGet** com argumento GL \_ descompactar \_ ignorar \_ pixels

**glGet** com alinhamento do argumento GL \_ desembalar \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





