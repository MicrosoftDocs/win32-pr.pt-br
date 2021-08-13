---
description: Fornece informações específicas do Schannel sobre um contexto de segurança.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Consultando os atributos de um contexto Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f00f6d5f0660bbb3a0d4ce5890ab415325707dbda4087d025a010efdb3fd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919935"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Consultando os atributos de um contexto Schannel

A [**função QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fornece informações específicas de Schannel sobre um [*contexto de segurança*](../secgloss/s-gly.md). A maioria das informações é originalmente especificada quando o contexto é criado usando a função [**client InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ou o servidor [**AcceptSecurityContext (Schannel).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Algumas informações são especificadas ao obter um handle para a credencial usada para criar o contexto. Para obter mais informações, [consulte Obtendo credenciais Schannel](obtaining-schannel-credentials.md).

 

 
