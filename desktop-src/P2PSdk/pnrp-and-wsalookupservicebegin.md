---
description: O PNRP usa a função WSALookupServiceBegin para iniciar o processo que permite que um aplicativo faça o seguinte.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP e WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a90bee9e2979f80464b05a3f2891cc7d3cc8e1fa10fe33faefb7319940e321f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553396"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP e WSALookupServiceBegin

O PNRP usa [**a função WSALookupServiceBegin**](winsock-nsp-reference-links.md) para iniciar o processo que permite que um aplicativo faça o seguinte:

-   [Resolvendo um nome](#resolving-a-name)
-   [Enumerando nuvens de rede](#enumerating-network-clouds)

Os clientes que tentam executar uma das funções usam as funções [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** e **WSALookupServiceEnd.**

Usando [**WSANSPIoctl,**](winsock-nsp-reference-links.md)o serviço de lookup pode ser usado de forma assíncrona. Para obter informações sobre como usar as funções de serviço de busca de forma assíncrona, consulte [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).

O processo para trabalhar com nomes de pares é diferente de trabalhar com nuvens. Cada processo é descrito separadamente neste tópico.

## <a name="resolving-a-name"></a>Resolvendo um nome

Um aplicativo usa [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para obter o endereço IP, a porta e o protocolo para um serviço par registrado em outro computador. A **função WSALookupServiceBegin** é usada para iniciar o processo de resolução de nomes e configurar os parâmetros e restrições. Um handle é retornado e deve ser usado ao chamar **WSALookupServiceNext** e **WSANSPIoctl**.

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Ao resolver um nome par, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRestrictions* faz referência deve conter os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**Dwsize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**Lpszserviceinstancename**
</dt> <dd>

Especifica um nome de par a ser resolvido.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve ser **SVCID \_ PNRPNAME.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reservado, deve ser **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reservado, deve ser **NULL.**

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

Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL.** Se esse valor for **NULL ou** uma cadeia de caracteres vazia, a nuvem padrão" "Global" \_ será usada. Caso contrário, ele deverá apontar para um nome de nuvem válido.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reservado, deve ser **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**Lpcsabuffer**
</dt> <dd>

Reservado, deve ser **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**Lpblob**
</dt> <dd>

Deve ser um ponteiro para uma estrutura [**BLOB**](winsock-nsp-reference-links.md) ou **NULL.** Se for **NULL,** os valores padrão serão usados. Se estiver definido, **lpBlob** aponta para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) e parâmetros específicos na estrutura **PNRPINFO** devem ser definidos. Para obter mais informações, consulte as descrições a seguir para a estrutura PNRPINFO.

</dd> </dl>

Estrutura PNRPINFO

Se o **membro lpBlob** da estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) for definido, os seguintes membros da estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) deverão ser definidos:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**Dwsize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Reservado, deve ser **NULL.**

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Especifica o número solicitado de resoluções.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**Dwtimeout**
</dt> <dd>

Especifica o período de tempo de tempo de espera solicitado para aguardar respostas. O padrão é 30 segundos. O máximo é de 600 segundos (10 minutos).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Deve ser um dos valores permitidos. O padrão é **PNRP \_ RESOLVE CRITERIA NON CURRENT PROCESS PEER \_ \_ \_ \_ \_ \_ NAME**. Os valores válidos são especificados por [**CRITÉRIOS \_ DE RESOLUÇÃO \_ PNRP.**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**Dwflags**
</dt> <dd>

Deve ser zero (0) ou **PNRPINFO \_ HINT.** O padrão é zero (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Especifica o endereço IP da dica. A dica é usada ao tentar encontrar o nome do par mais próximo. O formato da dica é um endereço IPv6. Se **saHint** não for especificado ao localizar o nome de par mais próximo, um endereço IPv6 do computador local será usado. Esse membro será ignorado se **dwFlags** não estiver definido.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>Dwcontrolflags

Os seguintes sinalizadores LUP \_ RETURN \_ \* são suportados pelo PNRP:



| Valor                | Descrição                                |
|----------------------|--------------------------------------------|
| LUP \_ RETURN \_ NAME    | Retorna um nome e um contexto.                |
| LUP \_ RETURN \_ COMMENT | Retorna um comentário associado a um nome.  |
| LUP \_ RETURN \_ ADDR    | Retorna um endereço associado a um nome. |



 

## <a name="enumerating-network-clouds"></a>Enumerando nuvens de rede

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Ao enumerar nuvens, a [**estrutura LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o *parâmetro lpqsRestrictions* faz referência deve conter os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**Dwsize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**Lpszserviceinstancename**
</dt> <dd>

Deve ser **NULL.**

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve ser **SVCID \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reservado, deve ser **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reservado, deve ser **nulo**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Deve ser **ns \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Deve ser o **\_ provedor NS \_ PNRPCLOUD** ou **nulo**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Reservado, deve ser **nulo**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reservado, deve ser **nulo**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reservado, deve ser **nulo**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) . Se **lpBlob** for **NULL**, todas as nuvens serão enumeradas.

</dd> </dl>

Estrutura PNRPCLOUDINFO

Ao enumerar nuvens, os seguintes membros da estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) devem ser definidos:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Nuvem**
</dt> <dd>

Aponta para uma estrutura que especifica os critérios que você pode usar para filtrar os resultados da pesquisa. O membro **Cloud. Scope** pode ser **\_ \_ um escopo PNRP**, **\_ \_ escopo global PNRP**, **\_ \_ \_ escopo local do site PNRP** ou **\_ \_ \_ escopo local do link do PNRP**. Se **o \_ escopo \_ PNRP** for especificado, todas as nuvens serão retornadas. Caso contrário, somente nuvens que correspondam à **nuvem. Scope** serão retornadas.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**encloudstate**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

Os seguintes \_ sinalizadores de retorno Lup \_ \* são suportados pelo PNRP:



| Valor             | Descrição                                                       |
|-------------------|-------------------------------------------------------------------|
| LUP \_ nome de retorno \_ | Retorna um nome e um contexto.                                       |
| \_blob de retorno de Lup \_ | Retorna o [blob](pnrp-and-blob.md) associado a essa nuvem. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Códigos de erro NSP PNRP](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



