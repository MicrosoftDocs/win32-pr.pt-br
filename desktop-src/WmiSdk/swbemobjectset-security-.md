---
description: A \_ Propriedade Security do objeto SWbemObjectSet é usada para obter ou definir as configurações de segurança para um objeto SWbemObjectSet. Essa propriedade é um objeto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Propriedade SWbemObjectSet.Security_ (Wbemdisp. h)
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
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762322"
---
# <a name="swbemobjectsetsecurity_-property"></a>Propriedade SWbemObjectSet. Security \_

A **propriedade \_ Security** do objeto [**SWbemObjectSet**](swbemobjectset.md) é usada para obter ou definir as configurações de segurança para um objeto **SWbemObjectSet** . Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Definir a [**propriedade \_ Security**](swbemobject-security-.md) de um objeto [**SWbemObjectSet**](swbemobjectset.md) como **NULL** concede acesso ilimitado a todos os momentos. Para obter mais informações sobre as implicações de acesso ilimitado, consulte [**SWbemSecurity**](swbemsecurity.md).

 

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

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
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | ISWbemObjectSet de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Protegendo clientes de script](securing-scripting-clients.md)
</dt> </dl>

 

 




