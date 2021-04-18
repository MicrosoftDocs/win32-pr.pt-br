---
description: O PNRP usa a função WSALookupServiceBegin para iniciar o processo que permite que um aplicativo faça o seguinte.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP e WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105753114"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP e WSALookupServiceBegin

O PNRP usa a função [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para iniciar o processo que permite que um aplicativo faça o seguinte:

-   [Resolvendo um nome](#resolving-a-name)
-   [Enumerando nuvens de rede](#enumerating-network-clouds)

Os clientes que tentam executar uma das funções usam as funções [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** e **WSALookupServiceEnd** .

Usando [**WSANSPIoctl**](winsock-nsp-reference-links.md), o serviço de pesquisa pode ser usado de forma assíncrona. Para obter informações sobre como usar as funções de serviço de pesquisa de forma assíncrona, consulte [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).

O processo para trabalhar com nomes de pares é diferente de trabalhar com nuvens. Cada processo é descrito separadamente neste tópico.

## <a name="resolving-a-name"></a>Resolvendo um nome

Um aplicativo usa [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) para obter o endereço IP, a porta e o protocolo para um serviço de mesmo nível registrado em outro computador. A função **WSALookupServiceBegin** é usada para iniciar o processo de resolução de nomes e configurar os parâmetros e as restrições. Um identificador é retornado e deve ser usado ao chamar **WSALookupServiceNext** e **WSANSPIoctl**.

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Ao resolver um nome de par, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRestrictions* referencia deve conter os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Especifica um nome de par a ser resolvido.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve ser **SVCID \_ pnrpname**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reservado, deve ser **nulo**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reservado, deve ser **nulo**.

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

Deve ser um nome de nuvem, uma cadeia de caracteres vazia ou **NULL**. Se esse valor for **nulo** ou uma cadeia de caracteres vazia, a nuvem padrão, "global \_ ", será usada. Caso contrário, ele deve apontar para um nome de nuvem válido.

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

Deve ser um ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) ou **NULL**. Se for **NULL**, serão usados valores padrão. Se estiver definido, **lpBlob** apontará para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) e parâmetros específicos na estrutura **PNRPINFO** deverão ser definidos. Para obter mais informações, consulte as descrições a seguir para a estrutura PNRPINFO.

</dd> </dl>

Estrutura PNRPINFO

Se o membro **lpBlob** da estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) for definido, os seguintes membros da estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) deverão ser definidos:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Reservado, deve ser **nulo**.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Especifica o número solicitado de resoluções.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Especifica o período de tempo limite solicitado para aguardar respostas. O padrão é 30 segundos. O máximo é de 600 segundos (10 minutos).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Deve ser um dos valores permitidos. O padrão é **PNRP \_ resolve \_ o \_ \_ nome de \_ \_ par de \_ processo não atual**. Os valores válidos são especificados [**por \_ \_ critérios de resolução PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Deve ser zero (0) ou a **\_ dica PNRPINFO**. O padrão é zero (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Especifica o endereço IP para a dica. A dica é usada ao tentar localizar o nome de par mais próximo. O formato da dica é um endereço IPv6. Se **saHint** não for especificado ao localizar o nome de par mais próximo, será usado, em vez disso, um endereço IPv6 do computador local. Esse membro será ignorado se o **dwFlags** não estiver definido.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**Nome do seu**
</dt> <dd>

Reservado, deve ser zero (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

Os seguintes \_ sinalizadores de retorno Lup \_ \* são suportados pelo PNRP:



| Valor                | Descrição                                |
|----------------------|--------------------------------------------|
| LUP \_ nome de retorno \_    | Retorna um nome e um contexto.                |
| \_Comentário de retorno do Lup \_ | Retorna um comentário associado a um nome.  |
| \_endereço de retorno de Lup \_    | Retorna um endereço associado a um nome. |



 

## <a name="enumerating-network-clouds"></a>Enumerando nuvens de rede

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Ao enumerar nuvens, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) que o parâmetro *lpqsRestrictions* referencia deve conter os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Especifica o tamanho dessa estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Deve ser **NULL**.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Deve ser **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reservado, deve ser **nulo**.

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

 

 



