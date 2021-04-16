---
description: O PNRP usa a função WSALookupServiceNext para fazer a correspondência de consultas especificadas em uma chamada anterior para WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768450"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP e WSALookupServiceNext

O PNRP usa a função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para fazer a correspondência de consultas especificadas em uma chamada anterior para **WSALookupServiceBegin**. Os resultados da função **WSALookupServiceNext** são determinados pelas configurações na estrutura **WSAQUERYSET** passada na chamada de função **WSALookupServiceBegin** inicial. Essa função é usada para executar as duas funções a seguir:

-   Resolvendo um nome de par para uma lista de endereços
-   Enumerando nuvens de rede

Usando [**WSANSPIoctl**](winsock-nsp-reference-links.md), o serviço de pesquisa pode ser usado de forma assíncrona. Para obter informações sobre como usar as funções de serviço de pesquisa de forma assíncrona, consulte [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md).

A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) é bloqueada mesmo se **WSANSPIoctl** for chamado. Antes de chamar **WSALookupServiceNext**, um aplicativo deve aguardar até receber uma notificação — se o bloqueio for um problema.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Resolvendo um nome de par para uma lista de endereços

Ao resolver um nome de par para uma lista de endereços, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retornada no parâmetro *lpqsResults* contém os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Retorna o tamanho da estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Retorna um nome de par — **se \_ Lup \_ nome de retorno**, **Lup \_ retornar \_ tudo** ou **NULL** forem especificados.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Retorna **SVCID \_ pnrpname**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Retorna um comentário — se **Lup \_ retornar o \_ Comentário**, **Lup \_ retornará \_ All** ou **NULL** será especificado.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Retorna o **ns \_ pnrpname**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Retorna **o \_ provedor NS \_ pnrpname**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Retorna o nome da nuvem **se \_ Lup \_ nome de retorno**, **Lup \_ retornar \_ tudo** ou **NULL** forem especificados.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Retorna o número de entradas na matriz de \_ informações de CSADDR se **Lup \_ retornar \_ addr**, **Lup \_ retornar \_ todos** ou **NULL** forem especificados. Esse valor e as informações em **lpcsaBuffer** são os principais bits de informações retornados nessa estrutura.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Retorna um ponteiro para uma matriz de \_ estruturas de informações CSADDR se **Lup \_ retornar \_ addr**, **Lup \_ retornar \_ todos** ou **NULL** forem especificados. Esse buffer e o valor em **dwNumberOfCsAddrs** são os principais bits de informações retornados nessa estrutura.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Retorna **NULL**.

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Enumerando nuvens de rede

Ao enumerar nuvens, a estrutura [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retornada no parâmetro *lpqsResults* contém os seguintes valores:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Retorna o tamanho da estrutura.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Retorna um nome de nuvem — **se \_ Lup \_ nome de retorno**, **Lup \_ retornar \_ tudo** ou **NULL** forem especificados.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Retorna **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Retorna **ns \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Retorna **\_ \_ PNRPCLOUD do provedor NS**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Retorna **NULL**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Retorna zero (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Retorna um ponteiro para uma estrutura de [**blob**](winsock-nsp-reference-links.md) que aponta para uma estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) – se **Lup \_ retornar \_ blob**, **Lup \_ retornará \_ All** ou **null** será especificado.

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Estrutura PNRPCLOUDINFO

Ao enumerar nomes de nuvem, os seguintes valores são retornados na estrutura [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Nuvem**
</dt> <dd>

O valor real da nuvem.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**encloudstate**
</dt> <dd>

O estado atual de uma nuvem. [**PNRP \_ \_Estado da nuvem**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) especifica os valores válidos.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Indica que um nome de nuvem é válido em uma rede ou somente válido em um computador atual. [**PNRP \_ \_Sinalizadores de nuvem**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) especifica os valores válidos. Alguns nomes de nuvem são válidos em qualquer computador na mesma rede. Outros nomes de nuvem são válidos somente em um computador atual e podem ser válidos somente por um período de tempo.

-   Se **enCloudFlags** for definido como **\_ nome de nuvem PNRP \_ \_ local,** o nome só será válido localmente.
-   Se **enCloudFlags** não for definido, o nome da nuvem poderá ser transferido para outros computadores.

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

[Códigos de erro NSP PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceBegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



