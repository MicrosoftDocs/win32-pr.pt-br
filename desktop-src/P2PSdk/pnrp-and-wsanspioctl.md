---
description: O PNRP usa a função WSANSPIoctl para receber notificações sobre as alterações a seguir.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP e WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cc07415fb483e75af8d836274d45a2c53f205e3aae15f893f909d2363c0d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553306"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP e WSANSPIoctl

O PNRP usa [**a função WSANSPIoctl**](winsock-nsp-reference-links.md) para receber notificações sobre as alterações a seguir:

-   Uma lista de nuvem de rede
-   Disponibilidade dos resultados de uma solicitação de resolução de nomes

A primeira chamada para [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) define o tipo de informação sobre o qual um cliente é notificado. Um cliente pode ser notificado com uma mensagem Windows, uma rotina de conclusão, um identificador para um objeto WSAEVENT ou uma porta. Para obter mais informações sobre opções e definir *o parâmetro lpCompletion,* consulte **WSANSPIoctl**.

Para continuar recebendo notificações após uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md), um aplicativo deve chamar **WSANSPIoctl** novamente.

A [**função WSALookupServiceNext**](winsock-nsp-reference-links.md) bloqueia mesmo que **WSANSPIoctl** seja chamado. Antes de **chamar WSALookupServiceNext**, um aplicativo deve aguardar até receber uma notificação — se o bloqueio for um problema.

Ao chamar essa função, os parâmetros devem ter os seguintes valores:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*Proch*
</dt> <dd>

Especifica o handle que [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) retorna.

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Deve ser **SIO \_ NSP \_ NOTIFY \_ CHANGE.**

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*Lpvinbuffer*
</dt> <dd>

Deve ser **NULL.**

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*Cbinbuffer*
</dt> <dd>

Deve ser zero (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*Lpvoutbuffer*
</dt> <dd>

Deve ser **NULL.**

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Deve ser zero (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*Lpcbbytesreturned*
</dt> <dd>

Deve ser **NULL.**

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Especifica NULL **ou** um ponteiro para uma [**estrutura WSACOMPLETION.**](winsock-nsp-reference-links.md)

</dd> </dl>

Depois que uma notificação for recebida, chame [**WSALookupServiceNext**](winsock-nsp-reference-links.md) uma vez para obter os resultados.

Para encerrar uma pesquisa, chame [**WSALookupServiceEnd.**](winsock-nsp-reference-links.md)

## <a name="resolution-notifications"></a>Notificações de resolução

Um cliente pode ser notificado sempre que uma entrada de resolução de nome é adicionada. Em seguida, o [**cliente chama WSALookupServiceNext**](winsock-nsp-reference-links.md) para obter os dados de resolução.

Se o cliente não usar essa técnica, uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md) poderá ser bloqueada até que o tempoout especificado ocorra.

## <a name="cloud-list-notifications"></a>Notificações de lista de nuvem

Um cliente pode ser notificado sempre que houver uma alteração em um conjunto de nuvens.

A [**função WSALookupServiceNext**](winsock-nsp-reference-links.md) retorna **WSA \_ E NO \_ \_ MORE** como um delimiter definido. O aplicativo cliente deve enumerar nuvens existentes até que essa mensagem seja retornada e, em seguida, usar um esquema de notificação para recuperar alterações subsequentes conforme elas ocorrem. Um aplicativo cliente também pode chamar **WSALookupServiceNext,** mas a chamada é bloqueada até que ocorra uma alteração.

A [**função WSALookupServiceNext**](winsock-nsp-reference-links.md) retorna uma nuvem em uma **estrutura WSAQUERYSET.** Um dos sinalizadores a seguir é retornado no **membro dwOutputFlags.**



| Valor               | Descrição                                             |
|---------------------|---------------------------------------------------------|
| O \_ RESULTADO É \_ ADICIONADO   | A nuvem retornada é adicionada.                    |
| O RESULTADO \_ É \_ ALTERADO | A nuvem retornada é alterada.                  |
| O \_ RESULTADO \_ É EXCLUÍDO | A nuvem retornada é excluída e não é válida. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[Códigos de erro de NSP pnrp](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**Wsalookupservicebegin**
</dt> <dt>

**Wsalookupserviceend**
</dt> <dt>

**Wsaqueryset**
</dt> </dl>

 

 



