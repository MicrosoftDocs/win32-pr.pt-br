---
description: A propriedade Security do objeto SWbemObjectSet é usada para obter ou definir as configurações de segurança para um \_ objeto SWbemObjectSet. Essa propriedade é um objeto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: SWbemObjectSet.Security_ propriedade (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7e0725fc6aa35043a3a40220b1fb43a3624cfd6ef5b55775adf5f41d26fafe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857206"
---
# <a name="swbemobjectsetsecurity_-property"></a>Propriedade SWbemObjectSet.Security \_

A **\_ propriedade Security** do [**objeto SWbemObjectSet**](swbemobjectset.md) é usada para obter ou definir as configurações de segurança para um **objeto SWbemObjectSet.** Essa propriedade é um [**objeto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> Definir a [**propriedade \_ Security**](swbemobject-security-.md) de um objeto [**SWbemObjectSet**](swbemobjectset.md) como **NULL** concede acesso ilimitado a todos o tempo todo. Para obter mais informações sobre as implicações de acesso ilimitado, consulte [**SWbemSecurity**](swbemsecurity.md).

 

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Proteger clientes de script](securing-scripting-clients.md)
</dt> </dl>

 

 




