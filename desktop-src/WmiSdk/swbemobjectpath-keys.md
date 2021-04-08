---
description: A propriedade Keys do objeto SWbemObjectPath é um objeto SWbemNamedValueSet que contém as associações de valor de chave. Esta propriedade é somente para leitura.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. Keys (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010761"
---
# <a name="swbemobjectpathkeys-property"></a>Propriedade SWbemObjectPath. Keys

A propriedade **Keys** do objeto [**SWbemObjectPath**](swbemobjectpath.md) é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contém as associações de valor de chave. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="error-codes"></a>Códigos do Erro

Depois de recuperar a propriedade **Keys** , o objeto **Err** pode conter o código de erro abaixo.

<dl> <dt>

**wbemErrNotSupported** -2147749900 (0x8004100C)
</dt> <dd>

Não há suporte para o recurso ou operação. Esse erro será retornado se um script tentar gravar nessa propriedade.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                             |
| parâmetro<br/>                   | <dl> <dt>Adoctint. h (incluir Wbemdisp. h)</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl>                    |
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                                          |
| IID<br/>                      | ISWbemObjectPath de IID \_<br/>                                                                           |



 

 




