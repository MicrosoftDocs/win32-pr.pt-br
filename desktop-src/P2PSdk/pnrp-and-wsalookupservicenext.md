---
description: O PNRP usa a função WSALookupServiceNext para corresponder às consultas especificadas em uma chamada anterior para WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec10c8021a2f13be1a1ffe228ca73a07c8af10dfc8714bef14f0bddeb0952aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553316"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP e WSALookupServiceNext

O PNRP usa a [**função WSALookupServiceNext**](winsock-nsp-reference-links.md) para corresponder às consultas especificadas em uma chamada anterior para **WSALookupServiceBegin.** Os resultados da **função WSALookupServiceNext** são determinados pelas configurações na estrutura **WSAQUERYSET** passadas na chamada de função **WSALookupServiceBegin** inicial. Essa função é usada para executar as duas funções a seguir:

-   Resolvendo um nome par para uma lista de endereços
-   Enumerando nuvens de rede

Usando [**WSANSPIoctl,**](winsock-nsp-reference-links.md)o serviço de lookup pode ser usado de forma assíncrona. Para obter informações sobre como usar as funções de serviço de busca de forma assíncrona, consulte [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).

A [**função WSALookupServiceNext**](winsock-nsp-reference-links.md) bloqueia mesmo que **WSANSPIoctl** seja chamado. Antes de **chamar WSALookupServiceNext**, um aplicativo deve aguardar até receber uma notificação — se o bloqueio for um problema.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Resolvendo um nome par para uma lista de endereços

Ao resolver um nome par para uma lista de endereços, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retornada no parâmetro *lpqsResults* contém os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**Dwsize**
</dt> <dd>

Retorna o tamanho da estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**Lpszserviceinstancename**
</dt> <dd>

Retorna um nome de par — se **LUP \_ RETURN \_ NAME**, **LUP \_ RETURN \_ ALL** ou **NULL** são especificados.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Retorna **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Retorna um comentário – se **LUP \_ RETURN \_ COMMENT**, **LUP \_ RETURN \_ ALL** ou **NULL** são especificados.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**Dwnamespace**
</dt> <dd>

Retorna **NS \_ PNRPNAME.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Retorna **NS \_ PROVIDER \_ PNRPNAME**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Retorna o nome da nuvem **se LUP \_ RETURN \_ NAME**, **LUP RETURN \_ \_ ALL** ou **NULL** são especificados.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Retorna o número de entradas na matriz DE INFORMAÇÕES CSADDR se \_ **LUP \_ RETURN \_ ADDR,** **LUP \_ RETURN \_ ALL** ou **NULL** são especificados. Esse valor e as informações em **lpcsaBuffer** são os principais bits de informações retornadas nessa estrutura.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**Lpcsabuffer**
</dt> <dd>

Retorna um ponteiro para uma matriz de estruturas INFO CSADDR se \_ **LUP \_ RETURN \_ ADDR**, **LUP \_ RETURN \_ ALL** ou **NULL** são especificados. Esse buffer e o valor em **dwNumberOfCsAddrs** são os bits de informações principais retornados nessa estrutura.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**Lpblob**
</dt> <dd>

Retorna **NULL.**

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Enumerando nuvens de rede

Ao enumerar nuvens, a estrutura [**LPWSAQUERYSET retornada**](pnrp-and-wsaqueryset.md) no parâmetro *lpqsResults* contém os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**Dwsize**
</dt> <dd>

Retorna o tamanho da estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**Lpszserviceinstancename**
</dt> <dd>

Retorna um nome de nuvem – se **LUP \_ RETURN \_ NAME**, **LUP \_ RETURN \_ ALL** ou **NULL** são especificados.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Retorna **SVCID \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**Dwnamespace**
</dt> <dd>

Retorna **NS \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Retorna **NS \_ PROVIDER \_ PNRPCLOUD.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**Lpcsabuffer**
</dt> <dd>

Retorna **NULL.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**Lpblob**
</dt> <dd>

Retorna um ponteiro para uma estrutura [**BLOB**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) – se **LUP \_ RETURN \_ BLOB**, **LUP \_ RETURN \_ ALL** ou **NULL** são especificados.

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Estrutura PNRPCLOUDINFO

Ao enumerar nomes de nuvem, os seguintes valores são retornados na estrutura [**PNRPCLOUDINFO:**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**Dwsize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Nuvem**
</dt> <dd>

O valor real da nuvem.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

O estado atual de uma nuvem. [**PNRP \_ CLOUD \_ STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) especifica os valores válidos.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Indica que um nome de nuvem é válido em uma rede ou válido somente em um computador atual. [**PNRP \_ CLOUD \_ FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) especifica os valores válidos. Alguns nomes de nuvem são válidos em qualquer computador na mesma rede. Outros nomes de nuvem são válidos somente em um computador atual e podem ser válidos apenas por um período.

-   Se **enCloudFlags** for definido como **PNRP \_ CLOUD NAME \_ \_ LOCAL,** o nome só será válido localmente.
-   Se **enCloudFlags não** estiver definido, o nome da nuvem poderá ser transferido para outros computadores.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PNRP e BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Códigos de erro de NSP pnrp](pnrp-nsp-error-codes.md)
</dt> <dt>

[**Wsalookupservicebegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



