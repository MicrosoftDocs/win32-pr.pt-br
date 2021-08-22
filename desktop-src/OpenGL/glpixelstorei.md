---
title: Função glPixelStorei (Gl.h)
description: Define os modos de armazenamento de pixel. | Função glPixelStorei (Gl.h)
ms.assetid: 1e1e94e9-aabe-4923-a0a9-f1c041a925ba
keywords:
- Função glPixelStorei OpenGL
topic_type:
- apiref
api_name:
- glPixelStorei
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8658db575bbc58cd7aa1170612895f7f895ccc22f11afdfdb99be90db44fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938171"
---
# <a name="glpixelstorei-function"></a>Função glPixelStorei

Define os modos de armazenamento de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelStorei(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

O nome simbólico do parâmetro a ser definido. Seis dos parâmetros de armazenamento afetam como os dados de pixel são retornados à memória do cliente e, portanto, são significativos apenas para [**comandos glReadPixels.**](glreadpixels.md) Eles são os que se seguem.



| Armazenamento Parâmetro                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BYTES DE \_ \_ TROCA DO PACOTE GL \_                                       | Se true, a ordenação de byte para componentes de cores multibyte, componentes de profundidade, índices de cores ou índices de estêncil será invertida. Ou seja, se um componente de quatro bytes for feito de bytes *b* 0 , *b* 1 , *b* 2 , *b* 3 , ele será armazenado na memória como *b* 3 , *b* 2 , *b* 1 , *b* 0 se GL PACK SWAP BYTES \_ for \_ \_ true. GL PACK SWAP BYTES não tem nenhum efeito na ordem de memória dos componentes dentro de um pixel, apenas na ordem de bytes dentro de \_ \_ \_ componentes ou índices. Por exemplo, os três componentes de um pixel de formato GL RGB são sempre armazenados com o primeiro vermelho, o segundo verde e o terceiro azul, independentemente do valor de \_ GL \_ PACK SWAP \_ \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                               |
| GL \_ PACK \_ LSB \_ FIRST                                        | Se true, os bits são ordenados dentro de um byte do menos significativo para o mais significativo; caso contrário, o primeiro bit em cada byte é o mais significativo. Esse parâmetro é significativo apenas para dados de bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| COMPRIMENTO DA \_ \_ LINHA DO PACOTE GL \_                                       | Se for maior que zero, GL \_ PACK \_ ROW LENGTH \_ definirá o número de pixels em uma linha. Se o primeiro pixel de uma linha for colocado no local p na memória, o local do primeiro pixel da próxima linha será obtido ignorando Equação mostrando o local do primeiro pixel da próxima linha em ![ GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ componentes ou índices newline, em que n é o número de componentes ou índices em um pixel, l é o número de pixels em uma linha (comprimento da linha gl pack se for maior que zero, o argumento de largura para a rotina de pixel caso contrário), um é o valor do alinhamento do pacote gl e s é o tamanho, em bytes, de um único componente \]   \- \- \-  \- (se \-    <     =  for , será como se fosse um ). no caso de valores de 1 bit, o local da próxima linha é obtido ignorando Equação mostrando o local da próxima linha em ![ GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> componentes ou índices. O componente *de palavra* nesta descrição refere-se aos valores de não índice vermelho, verde, azul, alfa e profundidade. Armazenamento formato GL RGB, por exemplo, tem três componentes por pixel: primeiro \_ vermelho, depois verde e, por fim, azul.<br/> |
| GL \_ PACK \_ SKIP \_ PIXELS e <br/> GL \_ PACK \_ SKIP \_ ROWS | Esses valores são fornecidos como uma conveniência para o programador; eles não fornecem nenhuma funcionalidade que não pode ser duplicada simplesmente incrementando o ponteiro passado para [**glReadPixels.**](glreadpixels.md) Definir GL PACK SKIP PIXELS como i é equivalente a incrementar o ponteiro por i n componentes ou \_ \_ \_ índices,    em que n é o número de componentes ou índices em cada pixel. Definir GL PACK SKIP ROWS como j é equivalente a incrementar o ponteiro por componentes ou índices j k, em que k é o número de componentes ou índices por linha, conforme calculado acima na seção COMPRIMENTO DE \_ \_ LINHA DO PACOTE \_    \_ \_ \_ GL.                                                                                                                                                                                                                                                                                                                                                                                                   |
| ALINHAMENTO DO PACOTE \_ \_ GL                                         | Especifica os requisitos de alinhamento para o início de cada linha de pixel na memória. Os valores acessíveis são 1 (alinhamento de bytes), 2 (linhas alinhadas a bytes numerados de mesmo tamanho), 4 (alinhamento de palavras) e 8 (linhas começam em limites de palavra dupla).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Os outros seis parâmetros de armazenamento afetam como os dados de pixel são lidos da memória do cliente. Esses valores são significativos para [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)e [**glPolygonStipple**](glpolygonstipple.md). Elas são as seguintes:



| Armazenamento Parâmetro                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BYTES DE \_ TROCA DE \_ DESEMPACOTAR \_ GL                                         | Se true, a ordenação de byte para componentes de cores multibyte, componentes de profundidade, índices de cores ou índices de estêncil será invertida. Ou seja, se um componente de quatro bytes for feito de bytes *b* 0 , *b* 1 , *b* 2 , *b* 3 , ele será armazenado na memória como *b* 3 , *b* 2 , *b* 1 , *b* 0 se GL UNPACK SWAP BYTES \_ for \_ \_ true. GL UNPACK SWAP BYTES não tem nenhum efeito na ordem de memória dos componentes dentro de um pixel, apenas na ordem de bytes dentro \_ \_ de \_ componentes ou índices. Por exemplo, os três componentes de um pixel de formato GL RGB são sempre armazenados com vermelho primeiro, segundo verde e terceiro azul, independentemente do valor de \_ BYTES SWAP DE GL \_ \_ \_ UNPACK.                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ UNPACK \_ LSB \_ FIRST                                          | Se true, os bits são ordenados dentro de um byte do menos significativo para o mais significativo; caso contrário, o primeiro bit em cada byte é o mais significativo. Isso é significativo apenas para dados de bitmap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| COMPRIMENTO DA \_ LINHA DE \_ DESEMPACOTAR \_ GL                                         | Se for maior que zero, GL \_ UNPACK \_ ROW LENGTH \_ definirá o número de pixels em uma linha. Se o primeiro pixel de uma linha for colocado no local p na memória, o local do primeiro pixel da próxima linha será obtido ignorando Equação mostrando o local do primeiro pixel da próxima linha em ![ GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ componentes ou índices newline, em que n é o número de componentes ou índices em um pixel, l é o número de pixels em uma linha (comprimento da linha gl pack se for maior que zero, o argumento de largura para a rotina de pixel caso contrário), um é o valor do alinhamento do pacote gl e s é o tamanho, em bytes, de um único componente \]   \- \- \-  \- (se \-    <     =  for , será como se fosse um ). no caso de valores de 1 bit, o local da próxima linha é obtido ignorando Equação mostrando o local da próxima linha em ![ GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> componentes ou índices. O componente *de palavra* nesta descrição refere-se aos valores de não índice vermelho, verde, azul, alfa e profundidade. Armazenamento formato GL RGB, por exemplo, tem três componentes por pixel: primeiro \_ vermelho, depois verde e, por fim, azul.<br/> |
| GL \_ UNPACK \_ IGNORE \_ PIXELS E <br/> GL \_ UNPACK \_ SKIP \_ ROWS | Esses valores são fornecidos como uma conveniência para o programador; eles não fornecem nenhuma funcionalidade que não possa ser duplicada simplesmente incrementando o ponteiro passado para [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)ou [**glPolygonStipple**](glpolygonstipple.md). Definir GL UNPACK SKIP PIXELS como i é equivalente a incrementar o ponteiro por i n componentes ou \_ \_ \_ índices,    em que n é o número de componentes ou índices em cada pixel. Definir GL UNPACK SKIP ROWS como j é equivalente a incrementar o ponteiro por índices ou componentes j k, em que k é o número de componentes ou índices por linha, conforme calculado acima na seção COMPRIMENTO DA LINHA \_ \_ GL \_    \_ \_ \_ UNPACK.                                                                                                                                                                                                                                    |
| ALINHAMENTO DE \_ DESEMPACOTAR \_ GL                                           | Especifica os requisitos de alinhamento para o início de cada linha de pixel na memória. Os valores acessíveis são 1 (alinhamento de bytes), 2 (linhas alinhadas a bytes numerados de mesmo tamanho), 4 (alinhamento de palavras) e 8 (linhas começam em limites de palavra dupla).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

O valor para *o que pname* está definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glPixelStore** define os modos de armazenamento de pixel que afetam a operação de [**glDrawPixels**](gldrawpixels.md) e [**glReadPixels subsequentes,**](glreadpixels.md) bem como a desempacotura de padrões de apple de polígono (consulte [**glPolygonStipple),**](glpolygonstipple.md)bitmaps (consulte [**glBitmap**](glbitmap.md)) e padrões de textura (consulte [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md)).

A tabela a seguir fornece o tipo, o valor inicial e o intervalo de valores válidos para cada um dos parâmetros de armazenamento que podem ser definidos com **glPixelStore**.



| Pname                    | Tipo    | Valor inicial | Intervalo Válido   |
|--------------------------|---------|---------------|---------------|
| BYTES DE \_ \_ TROCA DO PACOTE GL \_    | Boolean | false         | true ou false |
| BYTES DE \_ \_ TROCA DO PACOTE GL \_    | Boolean | false         | true ou false |
| COMPRIMENTO DA \_ \_ LINHA DO PACOTE GL \_    | inteiro | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ ROWS     | inteiro | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ PIXELS   | inteiro | 0             | \[0,?)        |
| ALINHAMENTO DO PACOTE \_ \_ GL      | Número inteiro | 4             | 1, 2, 4 ou 8 |
| \_bytes de permuta de descompactação GL \_ \_  | Boolean | false         | true ou false |
| GL \_ Unpack \_ LSB \_ primeiro   | Boolean | false         | true ou false |
| \_comprimento de linha de descompactação GL \_ \_  | inteiro | 0             | \[0,?)        |
| o GL \_ desembalar \_ ignora \_ linhas   | inteiro | 0             | \[0,?)        |
| o GL \_ desembalar \_ ignorar \_ pixels | inteiro | 0             | \[0,?)        |
| \_alinhamento de descompactação GL \_    | Número inteiro | 4             | 1, 2, 4 ou 8 |



 

A função [**glPixelStoref**](glpixelstoref.md) pode ser usada para definir qualquer parâmetro de armazenamento de pixel. Se o tipo de parâmetro for booliano e se *param* for 0,0, o parâmetro será false; caso contrário, ele será definido como true. Se *pname* for um parâmetro de tipo inteiro, *param* será arredondado para o número inteiro mais próximo.

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

 

 





