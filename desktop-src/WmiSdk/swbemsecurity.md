---
description: O objeto SWbemSecurity Obtém ou define as configurações de segurança, como privilégios, impessoas e níveis de autenticação atribuídos a um objeto.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Objeto SWbemSecurity (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768421"
---
# <a name="swbemsecurity-object"></a>Objeto SWbemSecurity

O objeto **SWbemSecurity** Obtém ou define as configurações de segurança, como privilégios, impessoas e níveis de autenticação atribuídos a um objeto. Os objetos [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)e [**SWbemEventSource**](swbemeventsource.md) têm uma propriedade **Security \_** , que é o objeto **SWbemSecurity** . Quando você recupera uma instância ou exibe o log de segurança do WMI, talvez seja necessário definir as propriedades do objeto de **segurança \_** .

A chamada do VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) não pode criar o objeto de segurança. As configurações de segurança nesse objeto não identificam as configurações de autenticação, representação ou privilégios em uma conexão com o WMI ou a segurança em vigor para o proxy quando um objeto é entregue a um coletor em uma chamada assíncrona. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

## <a name="members"></a>Membros

O objeto **SWbemSecurity** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **SWbemSecurity** tem essas propriedades.



| Propriedade                                                                    | Tipo de acesso           | Description                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)<br/> | Leitura/gravação<br/> | Valor numérico que define o nível de autenticação COM que é atribuído a esse objeto. Essa configuração determina como você protege as informações enviadas do WMI.<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | Leitura/gravação<br/> | Valor numérico que define o nível de representação COM que é atribuído a esse objeto. Essa configuração determina se os processos de propriedade da WMI podem detectar ou usar suas credenciais de segurança ao fazer chamadas para outros processos.<br/> |
| [**Direitos**](swbemsecurity-privileges.md)<br/>                   | Somente leitura<br/>  | Um objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) que define privilégios para esse objeto. Para obter mais informações, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSECURITY CLSID<br/>                                                         |
| IID<br/>                      | ISWbemSecurity de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> <dt>

[Definindo a \_ segurança do processo do aplicativo cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

