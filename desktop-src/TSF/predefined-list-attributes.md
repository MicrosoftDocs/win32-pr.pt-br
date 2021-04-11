---
title: Atributos de lista predefinidos (TsAttrid. h)
description: Os valores a seguir identificam os atributos de lista obtidos com o método ITfContext GetAppProperty. O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Atributos de lista predefinidos estrutura de serviços de texto
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086124"
---
# <a name="predefined-list-attributes"></a>Atributos de lista predefinidos

Os valores a seguir identificam os atributos de lista obtidos com o método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . O formato de dados e o conteúdo de cada tipo de propriedade são incluídos.

## <a name="properties"></a>Propriedades



| Propriedade                          | Descrição                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| Lista de TSATTRID \_                    | Não usado.                                                                                       |
| TSATTRID \_ lista \_ LevelIndel        | Contém o nível de índice da lista. 1 é o nível mais externo, 2 é o próximo nível e assim por diante. |
| \_Tipo de lista TSATTRID \_              | Não usado.                                                                                       |
| \_Tipo de lista TSATTRID \_ \_ árabe      | Contém um valor diferente de zero se a lista for uma lista de algarismos árabes ou zero caso contrário.               |
| \_Marcador de \_ tipo de lista de TSATTRID \_      | Contém um valor diferente de zero se a lista for uma lista com marcadores ou zero caso contrário.                      |
| TSATTRID \_ tipo de lista \_ \_ LowerLetter | Contém um valor diferente de zero se a lista for uma lista de letras minúsculas ou zero caso contrário.            |
| TSATTRID \_ tipo de lista \_ \_ LowerRoman  | Contém um valor diferente de zero se a lista for uma lista de algarismos romanos minúsculos ou zero caso contrário.       |
| TSATTRID \_ tipo de lista \_ \_ UpperLetter | Contém um valor diferente de zero se a lista for uma lista com letras maiúsculas ou zero caso contrário.          |
| TSATTRID \_ tipo de lista \_ \_ UpperRoman  | Contém um valor diferente de zero se a lista for uma lista de algarismos romanos maiúsculos ou zero caso contrário.      |



 

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

 

