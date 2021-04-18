---
description: Recupera a senha da conta de serviço.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Função GetServiceAccountPassword (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767812"
---
# <a name="getserviceaccountpassword-function"></a>Função GetServiceAccountPassword

Recupera a senha da conta de serviço, disponível para os SSPs ( [*provedores de suporte de segurança*](/windows/desktop/SecGloss/s-gly) ), como o SSP do Kerberos.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AccountName* \[ no\]
</dt> <dd>

Nome da conta terminada com nulo da conta de conta de serviço gerenciado (gMSA) do grupo. O nome de usuário pode ser uma das seguintes formas:

-   Nome da conta SAM do gMSA.
-   Nome de usuário em um FQDN (nome de domínio totalmente qualificado), como *DomainName * **\\** _username_ ou **www.** _domínio_* do _. com \\_ * _nome_. O nome de usuário deve ser apenas um nome SAM. O nome de domínio pode ser um nome DNS ou um nome NetBIOS.
-   UPN (nome principal de usuário) implícito para a conta gMSA, por exemplo, *somename * **@** _Domain_*_. com_*, em que, de acordo com a definição de um UPN implícito, o *domínio * * *. com** é o nome DNS de domínio real.

</dd> <dt>

*Nome_do_domínio* \[ em, opcional\]
</dt> <dd>

Nome de domínio opcional finalizado por nulo. Isso será válido somente se o parâmetro *AccountName* for um nome de conta Sam. O nome de domínio só pode ser um nome NetBIOS ou um FQDN (nome de domínio totalmente qualificado).

</dd> <dt>

*CredFetch* \[ no\]
</dt> <dd>

Um valor da enumeração [**de \_ busca de credenciais**](cred-fetch.md) que especifica como recuperar a credencial.



| Valor                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**CredFetchDefault**</dt> </dl> | O sistema operacional primeiro tenta recuperar a senha do cache local se não for o momento de buscar a senha. Se for o momento de buscar a senha, o sistema operacional entrará em contato com o controlador de domínio, caso contrário, retornará qualquer senha armazenada em cache com um valor de status êxito.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**CredFetchDPAPI**</dt> </dl>         | Retorna a credencial DPAPI local para o chamador. Os SSPs geralmente não exigem o uso desse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**CredFetchForced**</dt> </dl>     | Força o sistema operacional a tentar ler a senha do controlador de domínio. Durante a hora de substituição da senha, a senha pode ter sido alterada no controlador de domínio e em outros hosts membros, mas o host membro do gMSA reconhece a senha como ainda válida. Isso pode acontecer devido a problemas de distorção de relógio entre diferentes controladores de domínio. Quando esse valor é especificado, o sistema operacional determina se pode haver uma possível alteração de senha devido à distorção do relógio e, nesse caso, recupera a senha. Caso contrário, a credencial armazenada em cache será retornada. Se não houver nenhuma credencial armazenada em cache, o sistema operacional tentará obter uma do controlador de domínio.<br/> |



 

</dd> <dt>

*FileTimeExpiry* \[ entrada, saída, opcional\]
</dt> <dd>

Na entrada, se esse valor for não nulo e não for um **FILETIME** zero, *FileTimeExpiry* conterá o tempo de expiração das credenciais da conta de serviço como conhecido para o chamador. Se o parâmetro *FileTimeExpiry* for o mesmo que uma das credenciais atuais, essa chamada falhará. Na saída, o parâmetro *FileTimeExpiry* contém o tempo de expiração da credencial que está sendo retornada.

</dd> <dt>

*CurrentPassword* \[ fora\]
</dt> <dd>

A senha atual do gMSA.

</dd> <dt>

*PreviousPassword* \[ fora\]
</dt> <dd>

A senha anterior do gMSA.

</dd> <dt>

*FileTimeCurrPwdValidForOutbound* \[ out, opcional\]
</dt> <dd>

Indica o tempo após o qual a senha atual é válida para solicitações de saída. O chamador deve comparar a hora atual com esse valor e usar a senha atual retornada somente se a hora atual for maior ou igual ao valor retornado por esse parâmetro. O uso desse parâmetro é projetado para chamadores que não têm repetição na lógica de saída, por exemplo, NTLM.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.

Se a função falhar, o valor de retorno será um código NTSTATUS. Para obter mais informações, consulte [valores de retorno da função de política LSA](management-return-values.md).

Você pode usar a função [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) para converter o código NtStatus em um código de erro do Windows.

Quando você terminar de usar os buffers retornados nos parâmetros *CurrentPassword* e *PreviousPassword* , libere-os chamando a função [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .

## <a name="remarks"></a>Comentários

A função **GetServiceAccountPassword** pode ser chamada nos seguintes cenários:

-   Nas funções de logon do SSP (provedores de suporte de segurança), o SSP deve detectar que a senha da conta de serviço \_ \_ está sendo usada para fazer logon na entidade e verificar se o chamador tem privilégio TCB ou é um serviço de rede. Em seguida, o SSP deve permitir que o processo de logon continue obtendo a credencial mais recente chamando a função **GetServiceAccountPassword** com o valor **CredFetchDefault** na enumeração de [**\_ busca de cred**](cred-fetch.md) .

-   De SSPs em suas chamadas [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) e [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) . Os SSPs devem detectar que a \_ senha da conta de serviço \_ está sendo usada para essas chamadas e, se a chamada for para credenciais não primárias, o SSP deverá garantir que o chamador tenha o privilégio TCB ou seja um serviço de rede. Em seguida, o SSP deve chamar a função **GetServiceAccountPassword** com o valor **CredFetchDefault** na enumeração de [**\_ busca de cred**](cred-fetch.md) e prosseguir com a chamada. Se as chamadas **InitializeSecurityContext** e **AcceptSecurityContext** falharem, o SSP deverá usar o *FileTimeExpiry* recuperado da chamada anterior para **GetServiceAccountPassword** e usá-lo como entrada para chamar **GetServiceAccountPassword** novamente usando o valor **CredFetchForced** na enumeração **de \_ busca de credenciais** . Se uma nova credencial gMSA estiver disponível, a segunda chamada terá sucesso com novas credenciais, e o SSP deverá tentar novamente com as novas credenciais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

