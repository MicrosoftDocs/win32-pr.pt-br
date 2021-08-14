---
description: Fornece informações específicas do Schannel sobre uma credencial.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Consultando os atributos de uma credencial Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa940e6214f23a69af2e0f7de58813e007129caadac46be8a6c436b8d62094f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919905"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a>Consultando os atributos de uma credencial Schannel

A [**função QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fornece informações específicas de Schannel sobre uma credencial. Essas informações são originalmente especificadas quando a credencial é criada. Para obter mais informações, [consulte Obtendo credenciais Schannel](obtaining-schannel-credentials.md). As informações relatadas por essa função são válidas para quaisquer conexões ([*contextos de*](../secgloss/s-gly.md)segurança ) criadas usando a credencial especificada.

 

 
