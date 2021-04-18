---
description: O PNRP usa a função WSALookupServiceEnd para fazer o seguinte.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787479"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP e WSALookupServiceEnd

O PNRP usa a função [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) para fazer o seguinte:

-   Encerrar uma consulta iniciada em uma chamada anterior para [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)
-   Desbloquear uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para interromper a pesquisa

Uma chamada para [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) encerra uma consulta e limpa o contexto. O identificador obtido de uma chamada para **WSALookupServiceBegin** deve ser passado como um parâmetro para **WSALookupServiceEnd**.

Para obter mais informações sobre o PNRP e a função [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , consulte [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Códigos de erro NSP PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



