---
description: O PNRP usa a função WSANSPIoctl para receber notificações sobre alterações no seguinte.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP e WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753944"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP e WSANSPIoctl

O PNRP usa a função [**WSANSPIoctl**](winsock-nsp-reference-links.md) para receber notificações sobre as alterações feitas no seguinte:

-   Uma lista de nuvem de rede
-   Disponibilidade de resultados de uma solicitação de resolução de nomes

A primeira chamada para [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) define o tipo de informações sobre as quais um cliente é notificado. Um cliente pode ser notificado com uma mensagem do Windows, uma rotina de conclusão, um identificador para um objeto WSAEVENT ou uma porta. Para obter mais informações sobre as opções e definir o parâmetro *lpCompletion* , consulte **WSANSPIoctl**.

Para continuar recebendo notificações após uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md), um aplicativo deve chamar **WSANSPIoctl** novamente.

A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) é bloqueada mesmo se **WSANSPIoctl** for chamado. Antes de chamar **WSALookupServiceNext**, um aplicativo deve aguardar até receber uma notificação — se o bloqueio for um problema.

Ao chamar essa função, os parâmetros devem ter os seguintes valores:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*
</dt> <dd>

Especifica o identificador que [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) retorna.

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Deve ser **sio \_ NSP \_ notificar \_ alteração**.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Deve ser **NULL**.

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Deve ser zero (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Deve ser **NULL**.

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Deve ser zero (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Deve ser **NULL**.

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Especifica o **NULL** ou um ponteiro para uma estrutura [**WSACOMPLETION**](winsock-nsp-reference-links.md) .

</dd> </dl>

Depois que uma notificação for recebida, chame [**WSALookupServiceNext**](winsock-nsp-reference-links.md) uma vez para obter os resultados.

Para encerrar uma pesquisa, chame [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Notificações de resolução

Um cliente pode ser notificado sempre que uma entrada de resolução de nome for adicionada. Em seguida, o cliente chama [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para obter os dados de resolução.

Se o cliente não usar essa técnica, uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md) poderá ser bloqueada até que o tempo limite especificado ocorra.

## <a name="cloud-list-notifications"></a>Notificações da lista de nuvem

Um cliente pode ser notificado sempre que houver uma alteração em um conjunto de nuvens.

A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retorna **WSA \_ E \_ não \_ mais** como um delimitador de conjunto. O aplicativo cliente deve enumerar nuvens existentes até que essa mensagem seja retornada e, em seguida, usar um esquema de notificação para recuperar alterações subsequentes conforme elas ocorrem. Um aplicativo cliente também pode chamar **WSALookupServiceNext**, mas a chamada é bloqueada até que ocorra uma alteração.

A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retorna uma nuvem em uma estrutura **WSAQUERYSET** . Um dos sinalizadores a seguir é retornado no membro **dwOutputFlags** .



| Valor               | Descrição                                             |
|---------------------|---------------------------------------------------------|
| o resultado \_ é \_ adicionado   | A nuvem retornada é adicionada.                    |
| o resultado \_ é \_ alterado | A nuvem retornada é alterada.                  |
| o resultado \_ é \_ excluído | A nuvem retornada é excluída e não é válida. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[Códigos de erro NSP PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 



