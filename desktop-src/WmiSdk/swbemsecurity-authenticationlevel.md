---
description: A propriedade AuthenticationLevel é um inteiro que define o nível de Autenticação COM atribuído a esse objeto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity.AuthenticationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbb765241fabb86a14a5d74f7a839d5d81b017856b6da349b9ec04fd8535a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312710"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>Propriedade SWbemSecurity.AuthenticationLevel

A **propriedade AuthenticationLevel** é um inteiro que define o nível de Autenticação COM atribuído a esse objeto. Essa configuração determina como proteger as informações enviadas do WMI. Para obter mais informações sobre níveis de autenticação, consulte [Configurando a segurança do \_ processo de \_ aplicativo cliente.](setting-client-application-process-security.md) Em geral, não é necessário definir o nível de autenticação ao fazer chamadas à API WMI. Se você não definir essa propriedade, o nível de Autenticação COM padrão para o sistema será usado.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

A configuração authenticationLevel permite que você solicite o nível de autenticação e privacidade do DCOM a ser usado em toda uma conexão. Configurações intervalo de nenhuma autenticação a autenticação criptografada por pacote.



| Valor        | Descrição                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nenhum         | Não usa nenhuma autenticação. Todas as configurações de segurança são ignoradas.<br/>                                                                                                                                                                                                                                         |
| Padrão      | Usa uma negociação de segurança padrão para selecionar um nível de autenticação. Essa é a configuração recomendada porque o cliente envolvido na transação será negociado para o nível de autenticação especificado pelo servidor.<br/> O DCOM não selecionará o valor Nenhum durante uma sessão de negociação.<br/> |
| Conectar      | Autentica as credenciais do cliente somente quando o cliente tenta se conectar ao servidor. Depois que uma conexão tiver sido feita, nenhuma verificação de autenticação adicional ocorrerá.<br/>                                                                                                                          |
| Chamar         | Autentica as credenciais do cliente somente no início de cada chamada, quando o servidor recebe a solicitação. Os headers de pacote são assinados, mas os pacotes de dados trocados entre o cliente e o servidor não são assinados nem criptografados.<br/>                                                     |
| Pkt          | Autentica que todos os pacotes de dados são recebidos do cliente esperado. Semelhante à Chamada; Os headers de pacote são assinados, mas não criptografados. Os próprios pacotes não são assinados nem criptografados.<br/>                                                                                                               |
| PktIntegrity | Autentica e verifica se nenhum dos pacotes de dados transferidos entre o cliente e o servidor foi modificado. Cada pacote de dados é assinado, garantindo que os pacotes não tenham sido modificados durante o trânsito. Nenhum dos pacotes de dados é criptografado.<br/>                                            |
| PktPrivacy   | Autentica todos os níveis de representação anteriores e assina e criptografa cada pacote de dados. Isso garante que toda a comunicação entre o cliente e o servidor seja confidencial.<br/>                                                                                                                             |



 

Você pode definir o nível de autenticação dos objetos [**SWbemServices,**](swbemservices.md) [**SWbemObject**](swbemobject.md), [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) definindo a propriedade **AuthenticationLevel** como o valor desejado.

O exemplo a seguir mostra como definir o nível de autenticação para **um objeto SwbemObject.**


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



Você também pode especificar níveis de autenticação como parte de um moniker. O exemplo a seguir define o nível de autenticação e o nível de representação e recupera uma instância do [**\_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
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

[Definindo a segurança \_ do processo de aplicativo \_ cliente](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 

