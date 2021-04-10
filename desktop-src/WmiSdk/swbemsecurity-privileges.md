---
description: A propriedade Privileges é um objeto SWbemPrivilegeSet. Essa propriedade é usada para habilitar ou desabilitar privilégios específicos do Windows. Talvez seja necessário definir um desses privilégios para executar tarefas específicas usando a API Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity. Privileges (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165186"
---
# <a name="swbemsecurityprivileges-property"></a>Propriedade SWbemSecurity. Privileges

A propriedade **Privileges** é um objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) . Essa propriedade é usada para habilitar ou desabilitar privilégios específicos do Windows. Talvez seja necessário definir um desses privilégios para executar tarefas específicas usando a API Instrumentação de Gerenciamento do Windows (WMI).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Essa configuração permite conceder ou revogar privilégios como parte de uma cadeia de caracteres do moniker WMI. Para obter a lista completa de valores aplicáveis, consulte [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) e [**constantes de privilégio**](privilege-constants.md).

Você pode alterar os privilégios definidos para os objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) adicionando objetos [**SWbemPrivilege**](swbemprivilege.md) à propriedade **Privileges** .

Há diferenças fundamentais em como as diferentes versões do Windows lidam com os privilégios. Se você estiver desenvolvendo um aplicativo que só é usado em plataformas Windows, poderá definir ou revogar privilégios a qualquer momento.

O exemplo a seguir define o **SeDebugPrivilege** na conexão inicial do moniker para obter um objeto [**SWbemServices**](swbemservices.md) .


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Para obter mais informações sobre como formatar a cadeia de caracteres de segurança para uma conexão de moniker, consulte [**constantes de privilégio**](privilege-constants.md).

O exemplo a seguir executa a mesma tarefa, mas define o privilégio após o logon inicial no WMI.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Observe que, para chamadas para [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), você deve usar o nome completo do privilégio de segurança, por exemplo, "SeDebugPrivilege" em vez de "debug".

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

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> </dl>

 

 




