---
description: A propriedade ImpersonationLevel é um inteiro que define o nível de representação COM atribuído a esse objeto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity.ImpersonationLevel
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
ms.openlocfilehash: cde6bca09198d6e05f1ae0143ee07d1aedd465df68258303f1d6ca2b4b7699f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639576"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>Propriedade SWbemSecurity.ImpersonationLevel

A **propriedade ImpersonationLevel** é um inteiro que define o nível de representação COM atribuído a esse objeto. Essa configuração determina se os processos pertencentes Windows WMI (Instrumentação de Gerenciamento) podem detectar ou usar suas credenciais de segurança ao fazer chamadas para outros processos. Para obter mais informações sobre níveis de representação, consulte [Configurando a segurança do \_ processo de \_ aplicativo cliente.](setting-client-application-process-security.md)

Se você não definir o nível de representação especificamente em um moniker ou definindo a propriedade **SWBemSecurity.ImpersonationLevel** em um objeto securável, o WMI definirá o nível de representação padrão como o valor especificado na chave do Registro no nível de representação padrão [.](setting-the-default-process-security-level-using-vbscript.md) Se essa configuração não for suficiente, o provedor não adere à solicitação e a chamada para a API WMI poderá falhar com um código de erro **de wbemErrAccessDenied** (2147749891/0x80041003).

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Como um nível de representação DCOM, essa propriedade pode ser definida como um dos seguintes valores:



| Valor           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anônimo**   | Oculta as credenciais do autor da chamada. Na verdade, o WMI não dá suporte a esse nível de representação; se um script especificar impersonationLevel=Anonymous, o WMI atualizará silenciosamente o nível de representação para Identificar. Isso é de algumas maneiras um exercício sem sentido, no entanto, porque os scripts que usam o nível De identificação provavelmente falharão.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identificar**    | Permite que os objetos consultem as credenciais do chamador. Os scripts que usam esse nível de representação provavelmente falharão; O nível identificar normalmente permite que você não faça mais do que verificar listas de controle de acesso. Você não poderá executar scripts em computadores remotos usando Identificar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Permite que os objetos usem as credenciais do chamador. É recomendável usar esse nível de representação com scripts WMI. Quando você fizer isso, o script WMI usará suas credenciais de usuário; Como resultado, ele poderá executar todas as tarefas que você conseguir executar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegar**    | Permite que objetos permitam que outros objetos usem as credenciais do chamador. A delegação permite que um script use suas credenciais em um computador remoto e, em seguida, permite que o computador remoto use suas credenciais em outro computador remoto. Embora você possa usar esse nível de representação em scripts WMI, você deve fazer isso somente se necessário, pois isso pode representar um risco de segurança.<br/> Você não pode usar o nível de representação Delegado, a menos que todas as contas de usuário e contas de computador envolvidas na transação tenham sido marcadas como Confiáveis para delegação no Active Directory. Isso ajuda a minimizar os riscos de segurança. Embora um computador remoto possa usar suas credenciais, ele só poderá fazer isso se ele e quaisquer outros computadores envolvidos na transação são confiáveis para delegação.<br/> |



 

Conforme foi identificado, a representação anônima oculta suas credenciais e Identificar permite que um objeto remoto consulte suas credenciais, mas o objeto remoto não pode representar seu contexto de segurança. (Em outras palavras, embora o objeto remoto saiba quem você é, ele não pode "simular" ser você.) Scripts WMI que acessam computadores remotos usando uma dessas duas configurações geralmente falharão. Na verdade, a maioria dos scripts executados no computador local usando uma dessas duas configurações também falhará.

A representação permite que o serviço WMI remoto use seu contexto de segurança para executar a operação solicitada. Uma solicitação WMI remota que usa a configuração Representar normalmente é bem-sucedida, desde que suas credenciais tenham privilégios suficientes para executar a operação pretendido. Em outras palavras, você não pode usar o WMI para executar uma ação (remota ou de outra forma) que você não tem permissão para executar fora do WMI.

Definir impersonationLevel como Delegado permite que o serviço WMI remoto passe suas credenciais para outros objetos e geralmente é considerado um risco de segurança.

Você pode definir o nível de representação de um [**objeto SWbemServices,**](swbemservices.md) [**SWbemObject,**](swbemobject.md) [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) definindo a propriedade **ImpersonationLevel** como o valor desejado. O exemplo a seguir mostra como definir o nível de representação para um **objeto SWbemObject:**


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



Você também pode especificar níveis de representação como parte de um moniker. O exemplo a seguir define o nível de autenticação e o nível de representação e recupera uma instância do [**Serviço Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)


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
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Definindo a segurança \_ do processo de aplicativo \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

