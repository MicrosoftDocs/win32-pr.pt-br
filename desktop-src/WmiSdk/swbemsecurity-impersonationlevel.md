---
description: A propriedade ImpersonationLevel é um inteiro que define o nível de representação COM que é atribuído a esse objeto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity. ImpersonationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837251"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>Propriedade SWbemSecurity. ImpersonationLevel

A propriedade **ImpersonationLevel** é um inteiro que define o nível de representação com que é atribuído a esse objeto. Essa configuração determina se os processos pertencentes à Instrumentação de Gerenciamento do Windows (WMI) podem detectar ou usar suas credenciais de segurança ao fazer chamadas para outros processos. Para obter mais informações sobre os níveis de representação, consulte [definindo a \_ segurança do \_ processo do aplicativo cliente](setting-client-application-process-security.md).

Se você não definir o nível de representação especificamente em um moniker ou definindo a propriedade **SWBemSecurity. ImpersonationLevel** em um objeto protegível, o WMI definirá o nível de representação padrão como o valor especificado na [chave de registro de nível de representação padrão](setting-the-default-process-security-level-using-vbscript.md). Se essa configuração não for suficiente, o provedor não atenderá à sua solicitação e a chamada para a API do WMI poderá falhar com um código de erro de **wbemErrAccessDenied** (2147749891/0x80041003).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Como um nível de representação do DCOM, essa propriedade pode ser definida como um dos seguintes valores:



| Valor           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anônimo**   | Oculta as credenciais do autor da chamada. Na verdade, o WMI não dá suporte a esse nível de representação; se um script especificar impersonationLevel = Anonymous, o WMI atualizará silenciosamente o nível de representação para identificar. No entanto, isso é um exercício sem sentido, porque os scripts que usam o nível de identificação provavelmente falharão.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identificar**    | Permite que os objetos consultem as credenciais do chamador. Os scripts que usam esse nível de representação provavelmente falharão; o nível de identificação normalmente permite que você não faça mais do que verificar listas de controle de acesso. Você não poderá executar scripts em computadores remotos usando identificar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Permite que os objetos usem as credenciais do chamador. É recomendável que você use esse nível de representação com scripts WMI. Quando você fizer isso, o script WMI usará suas credenciais de usuário; Como resultado, será capaz de executar qualquer tarefa que você possa executar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegar**    | Permite que os objetos permitam que outros objetos usem as credenciais do chamador. A delegação permite que um script use suas credenciais em um computador remoto e, em seguida, permite que esse computador remoto use suas credenciais em outro computador remoto. Embora você possa usar esse nível de representação dentro de scripts WMI, você deve fazer isso somente se necessário, pois ele pode representar um risco de segurança.<br/> Você não pode usar o nível de representação de representante, a menos que todas as contas de usuário e contas de computador envolvidas na transação tenham sido marcadas como confiáveis para delegação em Active Directory. Isso ajuda a minimizar os riscos de segurança. Embora um computador remoto possa usar suas credenciais, ele pode fazer isso somente se ele e outros computadores envolvidos na transação forem confiáveis para delegação.<br/> |



 

Como observado, a representação anônima oculta suas credenciais e identifica permite que um objeto remoto consulte suas credenciais, mas o objeto remoto não pode representar o contexto de segurança. (Em outras palavras, embora o objeto remoto saiba quem você é, ele não pode "fingir" para você.) Os scripts WMI que acessam computadores remotos usando uma dessas duas configurações geralmente falharão. Na verdade, a maioria dos scripts executados no computador local usando uma dessas duas configurações também falhará.

Impersonate permite que o serviço WMI remoto use seu contexto de segurança para executar a operação solicitada. Uma solicitação WMI remota que usa a configuração Impersonate normalmente é realizada com sucesso, desde que suas credenciais tenham privilégios suficientes para executar a operação pretendida. Em outras palavras, você não pode usar o WMI para executar uma ação (remotamente ou de outra forma) que você não tem permissão para executar fora do WMI.

Definir impersonationLevel para delegar permite que o serviço WMI remoto passe suas credenciais para outros objetos e geralmente é considerado um risco de segurança.

Você pode definir o nível de representação de um objeto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) definindo a propriedade **ImpersonationLevel** para o valor desejado. O exemplo a seguir mostra como definir o nível de representação para um objeto **SWbemObject** :


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



Você também pode especificar os níveis de representação como parte de um moniker. O exemplo a seguir define o nível de autenticação e o nível de representação e recupera uma instância do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSECURITY CLSID<br/>                                                         |
| IID<br/>                      | ISWbemSecurity de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Definindo a \_ segurança do processo do aplicativo cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

