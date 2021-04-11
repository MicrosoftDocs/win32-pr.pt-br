---
description: Fornece informações específicas do Schannel sobre uma credencial.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Consultando os atributos de uma credencial Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169369"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a>Consultando os atributos de uma credencial Schannel

A função [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fornece informações específicas do Schannel sobre uma credencial. Essas informações são especificadas originalmente quando a credencial é criada. Para obter mais informações, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md). As informações relatadas por essa função são válidas para quaisquer conexões ([*contextos de segurança*](../secgloss/s-gly.md)) criadas usando a credencial especificada.

 

 
