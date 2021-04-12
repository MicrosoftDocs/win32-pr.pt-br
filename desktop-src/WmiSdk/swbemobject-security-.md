---
description: A \_ Propriedade Security do objeto SWbemObject é usada para ler ou definir as configurações de segurança para um objeto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297493"
---
# <a name="swbemobjectsecurity_-property"></a>Propriedade SWbemObject. Security \_

A **propriedade \_ Security** do objeto [**SWbemObject**](swbemobject.md) é usada para ler ou definir as configurações de segurança para um objeto **SWbemObject** . Essa propriedade é um objeto [**SWbemSecurity**](swbemsecurity.md) . As configurações de segurança nesse objeto não indicam as configurações de autenticação, representação ou privilégios feitas em uma conexão com Instrumentação de Gerenciamento do Windows (WMI) ou a segurança em vigor para o proxy quando um objeto é entregue a um coletor em uma chamada assíncrona. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

> [!Note]  
> Definir a **propriedade \_ Security** de um objeto [**SWbemObject**](swbemobject.md) como **NULL** concede acesso ilimitado a todos o tempo todo. Para obter mais informações, consulte [**SWbemSecurity**](swbemsecurity.md).

 

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.Security_ As Object
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Definindo a \_ segurança do processo do aplicativo cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilégio**](privilege-constants.md)
</dt> </dl>

 

 




