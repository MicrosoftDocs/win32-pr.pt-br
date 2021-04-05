---
title: Atributos de texto predefinidos (TsAttrid. h)
description: Os valores a seguir identificam os atributos de texto obtidos com o método ITfContext GetAppProperty. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.
ms.assetid: af73edb8-b706-40e4-a093-4ac22d33ecdc
keywords:
- Atributos de texto predefinidos estrutura de serviços de texto
topic_type:
- apiref
api_name:
- Predefined Text Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb214f6c555b589c52e9916325e38b46b0bfb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086123"
---
# <a name="predefined-text-attributes"></a>Atributos de texto predefinidos

Os valores a seguir identificam os atributos de texto obtidos com o método [**ITfContext:: GetAppProperty**](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.

## <a name="properties"></a>Propriedades



| Propriedade                                     | Descrição                                                                                                                                              |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Texto TSATTRID                               | Não usado.                                                                                                                                                |
| \_Alinhamento de texto TSATTRID \_                    | Não usado.                                                                                                                                                |
| \_Centro de \_ alinhamento de texto TSATTRID \_            | Contém um valor diferente de zero se o texto for centralizado ou for diferente de zero.                                                                                      |
| \_ \_ Justificar alinhamento de texto TSATTRID \_           | Contém um valor diferente de zero se o texto for justificado ou zero de outra forma.                                                                                     |
| \_Alinhamento de texto TSATTRID \_ \_ à esquerda              | Contém um valor diferente de zero se o texto estiver alinhado à esquerda ou zero de outra forma.                                                                                  |
| TSATTRID \_ alinhamento de texto \_ \_ à direita             | Contém um valor diferente de zero se o texto estiver alinhado à direita ou zero de outra forma.                                                                                 |
| TSATTRID \_ Text \_ inseridoobject               | Contém um valor diferente de zero se o texto for um objeto inserido ou nenhum outro.                                                                            |
| \_Hifenização de texto TSATTRID \_                  | Contém um valor diferente de zero se o texto for hifenizado ou zero caso contrário.                                                                                    |
| \_Linguagem de texto TSATTRID \_                     | Contém o identificador de idioma **LangID** do texto.                                                                                                 |
| \_Link de texto TSATTRID \_                         | Contém um ponteiro para um objeto de link. O chamador deve usar o método QueryInterface para obter a interface desejada, como **IUniformResourceLocator**. |
| TSATTRID \_ orientação do texto \_                  | Especifica o ângulo, em décimos de graus, entre a linha de base de texto e o eixo x do dispositivo.                                                          |
| TSATTRID \_ texto \_ para                         | Não usado.                                                                                                                                                |
| TSATTRID \_ Text \_ para \_ FirstLineIndent        | Contém o número de pontos que a primeira linha de um parágrafo é recuada.                                                                            |
| TSATTRID \_ Text \_ para \_ LeftIndent             | Contém o número de pontos que o parágrafo é recuado da esquerda.                                                                              |
| \_Texto TSATTRID \_ para \_ LineSpacing            | Não usado.                                                                                                                                                |
| TSATTRID \_ Text \_ para \_ LineSpacing no \_ mínimo   | Contém o número mínimo de linhas para o espaçamento de linha do parágrafo.                                                                              |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ Double    | Contém um valor diferente de zero se o parágrafo tem espaço duplo ou zero de outra forma.                                                                            |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ exatamente   | Contém o número exato de linhas para o espaçamento de linha do parágrafo.                                                                                |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ Multiple  | Contém o número de linhas para o espaçamento de várias linhas do parágrafo.                                                                             |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ OnePtFive | Contém um valor diferente de zero se o parágrafo é um e uma meia linha com espaçamento ou zero caso contrário.                                                             |
| TSATTRID \_ Text \_ para \_ LineSpacing \_ single    | Contém um valor diferente de zero se o parágrafo tem espaço único ou zero de outra forma.                                                                            |
| TSATTRID \_ Text \_ para \_ RightIndent            | Contém o número de pontos que o parágrafo é recuado a partir da direita.                                                                             |
| TSATTRID \_ Text \_ para \_ SpaceAfter             | Contém o número de pontos de espaçamento após o parágrafo.                                                                                            |
| TSATTRID \_ Text \_ para \_ SpaceBefore            | Contém o número de pontos de espaçamento antes do parágrafo.                                                                                           |
| \_Texto TSATTRID \_ ReadOnly                     | Contém zero se o texto for somente leitura ou não for diferente do contrário.                                                                                             |
| \_DireitaParaEsquerda de texto TSATTRID \_                  | Contém zero se o texto for de leitura da direita para a esquerda ou diferente do contrário.                                                                                 |
| \_VerticalWriting de texto TSATTRID \_              | Especifica se o texto é vertical ou horizontal. Contém zero se o texto for horizontal ou diferente de zero se o texto for vertical.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



 

