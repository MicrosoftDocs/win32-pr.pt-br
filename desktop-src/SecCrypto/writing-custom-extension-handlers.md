---
description: Para criar extensões personalizadas ou para codificar uma extensão complexa, você pode escrever seus próprios manipuladores de extensão que exportam interfaces personalizadas.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Gravando manipuladores de extensão personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796365"
---
# <a name="writing-custom-extension-handlers"></a>Gravando manipuladores de extensão personalizados

Para criar extensões personalizadas ou para codificar uma extensão complexa, você pode escrever seus próprios manipuladores de extensão que exportam interfaces personalizadas. Os serviços de certificados da Microsoft são fornecidos com as seguintes interfaces que podem ser usadas para codificar vários tipos de dados de extensão: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)e [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray). Essas interfaces estão contidas em Certenc.dll. Além disso, as informações de tipo para essas interfaces estão contidas no Certencl.dll, que está contido no SDK (Software Development Kit) da plataforma.

Para obter mais informações sobre manipuladores de extensão, consulte [manipuladores de extensão](extension-handlers.md).

 

 



