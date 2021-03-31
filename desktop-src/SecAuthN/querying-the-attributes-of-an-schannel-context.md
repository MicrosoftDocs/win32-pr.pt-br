---
description: Fornece informações específicas do Schannel sobre um contexto de segurança.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Consultando os atributos de um contexto Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089938"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Consultando os atributos de um contexto Schannel

A função [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fornece informações específicas do Schannel sobre um [*contexto de segurança*](../secgloss/s-gly.md). A maioria das informações é especificada originalmente quando o contexto é criado usando a função [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ou servidor [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) do cliente. Algumas informações são especificadas ao obter um identificador para a credencial usada para criar o contexto. Para obter mais informações, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).

 

 
