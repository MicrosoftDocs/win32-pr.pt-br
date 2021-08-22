---
description: O PNRP usa a função WSASetService para registrar ou remover nomes de par.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP e WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afbc11e65c9d583f91b5070e960435612ad05717b6ccfe087924da133c531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518096"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP e WSASetService

O PNRP usa a função [**WSASetService**](winsock-nsp-reference-links.md) para registrar ou remover [nomes de par](peer-names.md).

## <a name="registering-a-name"></a>Registrando um nome

O registro inclui um nome de par e um conjunto de pontos de extremidade onde um serviço pode ser contatado. Um registro é específico para uma nuvem PNRP. Depois que um par é registrado, há um atraso entre o registro e a propagação das informações de registro para outros nós. Durante esse tempo, outros nós podem não ser capazes de resolver um par registrado recentemente.

O registro do serviço não é persistente.

-   Se um processo de cliente que registra um nome de par sair ou chamar [**WSACleanup**](winsock-nsp-reference-links.md), o nome do par será cancelado.
-   Se um nome de par especificado já estiver registrado na mesma nuvem pelo processo atual, ele será substituído pelos novos valores de registro.

Ao registrar um nome de par, os seguintes valores de parâmetro devem ser indicados:

-   o parâmetro *essOperation* deve ter um valor **de \_ registro RNRSERVICE**.
-   o parâmetro *dwControlFlags* deve ser zero (0).

Ao registrar um nome de par, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) referenciada pelo parâmetro *lpqsRegInfo* deve conter os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica um nome de par a ser registrado. Se o [nome do par](peer-names.md) não for seguro, a identidade será opcional. Se a identidade for especificada como **nula**, o PNRP usará a identidade local do computador — por padrão.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve ser SVCID \_ pnrpname.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignorado. Defina como **nulo**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignorado. No entanto, a cadeia de caracteres ainda precisa ter menos de 40 caracteres, incluindo o terminador **nulo** .

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Deve ser **ns \_ pnrpname** ou **ns \_ All**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve ser o **\_ provedor NS \_ pnrpname** ou **NULL**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL**. Se esse valor for **nulo** ou uma cadeia de caracteres vazia, a nuvem padrão, "global", será usada. Caso contrário, ele deve apontar para um nome de nuvem válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignorado. Defina como zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignorado. Defina como **nulo**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Especifica o número de endereços registrados por um serviço. O número máximo de endereços que podem ser registrados para um único nome é 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Ponteiro para uma lista de endereços a serem registrados.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignorado. Defina como zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . Parâmetros específicos na estrutura **PNRPINFO** devem ser definidos. Para obter mais informações, consulte a seção de estrutura **PNRPINFO** a seguir.

</dd> </dl>

## <a name="pnrpinfo-structure"></a>Estrutura PNRPINFO

Se o membro **lpBlob** da estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) for definido, os seguintes membros da estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) deverão ser definidos:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Especifica a identidade do nome de par que é criado usando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Se um nome de par não for seguro, a identidade será opcional. Se a identidade for especificada como **nula**, o PNRP usará a identidade local do computador — por padrão.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Ignorado. Defina como zero (0).

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Ignorado. Defina como zero (0).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Especifica o número de segundos entre as operações de atualização.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Ignorado. Defina como zero (0).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Deve ser zero (0) ou a **\_ dica PNRPINFO**. O padrão é zero (0). Isso significa que a parte local do serviço da ID PNRP é criada usando o endereço IP em **saHint**. Caso contrário, o local do serviço é criado usando o primeiro endereço IP na primeira entrada IPv6 do membro **lpcsaBuffer** .

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Especifica o endereço IPv6 para a dica.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**Nome do seu**
</dt> <dd>

Ignorado. Defina como zero (0).

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Cancelando o registro de um nome de par

A lista a seguir identifica as informações importantes sobre o cancelamento do registro de um nome de par.

-   Somente um aplicativo que registra um nome de par pode cancelar seu registro.
-   Um nome de par será cancelado automaticamente se [**WSACleanup**](winsock-nsp-reference-links.md) for chamado.
-   O PNRP sempre remove o registro do nome do serviço inteiro. Ele não permite a remoção de endereços individuais.
-   Ao cancelar o registro de um nome, o parâmetro *essOperation* deve ter um valor de **RNRSERVICE \_ delete**.
-   O PNRP não oferece suporte ao valor **RNRSERVICE \_ cancelamento de registro**.
-   O parâmetro *dwControlFlags* deve ser zero (0).

Ao cancelar o registro de um nome, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRegInfo* referencia deve conter os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica um nome de par para cancelar o registro.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve ser **SVCID \_ PNRPNAME.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignorado. Definido como **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignorado. Definido como **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**Dwnamespace**
</dt> <dd>

Deve ser **NS \_ PNRPNAME ou** **NS \_ ALL.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve ser **NS \_ PROVIDER \_ PNRPNAME ou** **NULL.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL.** Se esse valor for **NULL ou** uma cadeia de caracteres vazia, a nuvem padrão" "Global" será usada. Caso contrário, ele deverá apontar para um nome de nuvem válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignorado. Definido como zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignorado. Definido como **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Ignorado. Definido como **NULL.**

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**Lpcsabuffer**
</dt> <dd>

Ignorado. Definido como **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignorado. Definido como zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**Lpblob**
</dt> <dd>

Ponteiro para uma [**estrutura BLOB**](winsock-nsp-reference-links.md) que aponta para uma [**estrutura PNRPINFO.**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) O **membro lpszIdentity** da estrutura **lpBlob** identifica o nome da identidade usada para registrar um nome de par. Os membros restantes devem ser definidos com os mesmos valores usados ao registrar um nome.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Códigos de erro de NSP pnrp](pnrp-nsp-error-codes.md)
</dt> <dt>

[**Wsacleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**Wsasetservice**
</dt> </dl>

 

 



