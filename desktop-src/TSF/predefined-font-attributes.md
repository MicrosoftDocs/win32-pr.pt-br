---
title: Atributos de fonte predefinidos (TsAttrid. h)
description: Os valores a seguir identificam os atributos de fonte obtidos com o método ITfContext GetAppProperty. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- Atributos de fonte predefinidos estrutura de serviços de texto
topic_type:
- apiref
api_name:
- Predefined Font Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21351d790a09c9364a101a62b7516698df154225
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295844"
---
# <a name="predefined-font-attributes"></a>Atributos de fonte predefinidos

Os valores a seguir identificam os atributos de fonte obtidos com o método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.

## <a name="properties"></a>Propriedades



| Propriedade                                                 | Descrição                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **\_Fonte TSATTRID**                                       | Não usado.                                                                                                                   |
| **\_Face da fonte TSATTRID \_**                             | Contém o nome da face da fonte do texto.                                                                                    |
| **TSATTRID \_ Font \_ SizePts**                              | Contém o tamanho do ponto da fonte do texto.                                                                                   |
| **\_Estilo de fonte TSATTRID \_**                                | Não usado.                                                                                                                   |
| **\_Animação de \_ estilo de fonte TSATTRID \_**                     | Não usado.                                                                                                                   |
| **\_BlinkingBackground de \_ animação de estilo de fonte TSATTRID \_ \_** | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_LasVegasLights de \_ animação de estilo de fonte TSATTRID \_ \_**     | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_MarchingBlackAnts de \_ animação de estilo de fonte TSATTRID \_ \_**  | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_MarchingRedAnts de \_ animação de estilo de fonte TSATTRID \_ \_**    | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_Shimmer de \_ animação de estilo de fonte TSATTRID \_ \_**            | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_SparkleText de \_ animação de estilo de fonte TSATTRID \_ \_**        | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_WipeDown de \_ animação de estilo de fonte TSATTRID \_ \_**           | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_WipeRight de \_ animação de estilo de fonte TSATTRID \_ \_**          | Contém um valor diferente de zero se o texto tiver a animação especificada ou zero de outra forma.                                         |
| **\_Estilo de fonte TSATTRID \_ \_ BackgroundColor**               | Contém o valor RGB do plano de fundo do texto. Contém 0xFF000000 se a cor do texto for automática.                          |
| **TSATTRID \_ de \_ estilo de fonte \_ piscada**                         | Contém um valor diferente de zero se o texto estiver piscando ou não em contrário.                                                         |
| **Estilo da fonte TSATTRID em \_ \_ \_ negrito**                          | Contém um valor diferente de zero se o texto for negrito ou zero do contrário.                                                             |
| **\_ \_ Capitalização de estilo de fonte TSATTRID \_**                    | Contém um valor diferente de zero se o texto estiver em maiúscula ou zero de outra forma.                                                      |
| **\_Cor do \_ estilo da fonte TSATTRID \_**                         | Contém o valor RGB da cor do texto. Contém 0xFF000000 se a cor do texto for automática.                               |
| **\_Entalhe de \_ estilo de fonte TSATTRID \_**                        | Contém um valor diferente de zero se o texto for em relevo ou zero de outra forma.                                                         |
| **Estilo de fonte TSATTRID de \_ \_ \_ baixo relevo**                       | Contém um valor diferente de zero se o texto for relevo ou zero caso contrário.                                                         |
| **\_Altura do \_ estilo da fonte TSATTRID \_**                        | Contém a altura da fonte. Para obter mais informações, consulte o membro **lfHeight** da estrutura LOGFONT.                       |
| **\_Estilo de fonte TSATTRID \_ \_ oculto**                        | Contém um valor diferente de zero se o texto estiver oculto ou zero caso contrário.                                                           |
| **\_ \_ Itálico estilo de fonte TSATTRID \_**                        | Contém um valor diferente de zero se o texto for itálico ou zero do contrário.                                                           |
| **\_ \_ Kerning de estilo de fonte TSATTRID \_**                       | Contém o tamanho mínimo de kerning. Para obter mais informações, consulte ITextFont:: getkerning.                                         |
| **\_Estilo de fonte TSATTRID \_ \_ minúscula**                     | Contém um valor diferente de zero se o texto for minúsculo ou nenhum outro.                                                        |
| **\_Estilo de fonte TSATTRID \_ \_ descrito**                      | Contém um valor diferente de zero se o texto for delineado ou zero caso contrário.                                                         |
| **\_Estilo de fonte TSATTRID \_ \_ linha sobreposta**                      | Contém um valor diferente de zero se o texto é sobrelinhado ou zero caso contrário.                                                        |
| **\_Estilo de fonte TSATTRID \_ \_ linha sobreposta \_ dupla**              | Contém um valor diferente de zero se o texto for duplo ondulado ou zero caso contrário.                                                 |
| **\_Estilo de fonte TSATTRID \_ \_ linha sobreposta \_ única**              | Contém um valor diferente de zero se o texto for de linha única ou zero de outra forma.                                                 |
| **\_Posição do \_ estilo da fonte TSATTRID \_**                      | Contém a posição da fonte.                                                                                                 |
| **\_Estilo de fonte TSATTRID \_ \_ protegido**                     | Contém um valor diferente de zero se o texto for protegido ou nenhum outro.                                                        |
| **\_Sombra do \_ estilo de fonte TSATTRID \_**                        | Contém um valor diferente de zero se o texto for sombreado ou for zero de outra forma.                                                         |
| **\_Estilo de fonte TSATTRID \_ \_ SmallCaps**                     | Contém um valor diferente de zero se o texto for minúsculo ou nenhum outro.                                                        |
| **\_ \_ Espaçamento do estilo da fonte TSATTRID \_**                       | Contém o espaçamento da fonte.                                                                                                  |
| **\_ \_ Tachado do estilo da fonte TSATTRID \_**                 | Não usado.                                                                                                                   |
| **\_Estilo de fonte TSATTRID \_ \_ tachado \_ duplo**         | Contém um valor diferente de zero se o texto estiver com Tachado Duplo ou zero caso contrário.                                             |
| **Estilo de fonte TSATTRID de \_ \_ \_ tachado \_ único**         | Contém um valor diferente de zero se o texto tiver um tachado simples ou nenhum outro.                                             |
| **Subscript de \_ estilo de fonte TSATTRID \_ \_**                     | Contém um valor diferente de zero se o texto for subscrito ou zero caso contrário.                                                        |
| **Superscript de \_ estilo de fonte TSATTRID \_ \_**                   | Contém um valor diferente de zero se o texto for sobrescrito ou zero caso contrário.                                                      |
| **\_Sublinhar estilo da fonte TSATTRID \_ \_**                     | Contém um valor diferente de zero se o texto for sublinhado ou zero caso contrário.                                                       |
| **\_Sublinhar estilo de fonte TSATTRID \_ \_ \_ duplo**             | Contém um valor diferente de zero se o texto for duplo sublinhado ou zero caso contrário.                                                |
| **\_Sublinhado do estilo de fonte TSATTRID \_ \_ \_ único**             | Contém um valor diferente de zero se o texto for um único sublinhado ou zero de outra forma.                                                |
| **TSATTRID \_ estilo da fonte em \_ \_ maiúsculas**                     | Contém um valor diferente de zero se o texto for maiúsculo ou zero de outra forma.                                                        |
| **\_Peso do \_ estilo da fonte TSATTRID \_**                        | Contém a espessura da fonte. Para obter mais informações sobre os valores possíveis, consulte o membro **lfWeight** da estrutura LOGFONT. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

