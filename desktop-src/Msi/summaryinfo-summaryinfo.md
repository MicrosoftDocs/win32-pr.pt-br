---
description: A Propriedade Property do objeto SummaryInfo define ou Obtém o valor para a propriedade especificada no fluxo de informações de resumo.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Propriedade SummaryInfo. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3b8635d081b44adfad3b3e869cb7fab96ee3d81107a8d962153f1caa5a14ac72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624084"
---
# <a name="summaryinfoproperty-property"></a>Propriedade SummaryInfo. Property

A propriedade **Property** do objeto [**SummaryInfo**](summaryinfo-object.md) define ou Obtém o valor para a propriedade especificada no fluxo de informações de resumo. As propriedades são lidas quando o objeto [**SummaryInfo**](summaryinfo-object.md) é criado, mas eles não são gravados até que o método [**Persist**](summaryinfo-persist.md) seja chamado. Definir uma propriedade como Empty causa sua remoção; da mesma forma, a solicitação de uma propriedade inexistente retorna um valor vazio. Caso contrário, os valores podem ser transferidos como cadeias de caracteres, inteiros ou tipos de data (data e hora).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Valor da propriedade

A ID de propriedade necessária de uma das propriedades de resumo.

## <a name="remarks"></a>Comentários

**IDs de propriedade de resumo padrão**

(não é uma enumeração)



| Nome do parâmetro     | Valor | Descrição                                       |
|--------------------|-------|---------------------------------------------------|
| \_dicionário PID    | 0     | Formato especial, não suporte pelo objeto SummaryInfo |
| \_página de código PID      | 1     | \_I2 VT                                            |
| título da PID \_         | 2     | a VT \_ LPSTR                                         |
| \_entidade PID       | 3     | a VT \_ LPSTR                                         |
| autor da PID \_        | 4     | a VT \_ LPSTR                                         |
| \_palavras-chave PID      | 5     | a VT \_ LPSTR                                         |
| Comentários de PID \_      | 6     | a VT \_ LPSTR                                         |
| \_modelo PID      | 7     | a VT \_ LPSTR                                         |
| DTI \_ LASTAUTHOR    | 8     | a VT \_ LPSTR                                         |
| DTI \_ REVNUMBER     | 9     | a VT \_ LPSTR                                         |
| PID \_ EditTime      | 10    | FILETIME do VT \_                                      |
| DTI \_ LASTPRINTED   | 11    | FILETIME do VT \_                                      |
| PID \_ criar \_ DTM   | 12    | FILETIME do VT \_                                      |
| DTI \_ LASTSAVE \_ DTM | 13    | FILETIME do VT \_                                      |
| DTI \_ PageCount     | 14    | \_I4 VT                                            |
| DTI \_ WORDCOUNT     | 15    | \_I4 VT                                            |
| DTI \_ charCount     | 16    | \_I4 VT                                            |
| miniatura de PID \_     | 17    | VT \_ CF (sem suporte)                            |
| \_APPNAME PID       | 18    | a VT \_ LPSTR                                         |
| segurança de PID \_      | 19    | \_I4 VT                                            |



 

**Tipos de dados de propriedade**

(não é uma enumeração)



| Nome do parâmetro | Valor | Descrição                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| \_I2 VT         | 2     | Inteiro de 16 bits                                                                           |
| \_I4 VT         | 3     | Inteiro de 32 bits                                                                           |
| a VT \_ LPSTR      | 30    | String                                                                                   |
| FILETIME do VT \_   | 64    | Data e hora (FILETIME, convertido em hora da variante)                                          |
| VT \_ CF         | 71    | Formato da área de transferência + dados, não manipulados pelo objeto [**SummaryInfo**](summaryinfo-object.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




