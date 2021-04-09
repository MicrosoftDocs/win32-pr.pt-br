---
description: Com um contexto orientado a conexão, o chamador da função é responsável por formatar mensagens. O chamador depende do pacote de segurança para autenticar conexões e garantir a integridade de partes específicas da mensagem.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Contextos de Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091323"
---
# <a name="connection-oriented-contexts"></a><span data-ttu-id="0cc9a-104">Contextos de Connection-Oriented</span><span class="sxs-lookup"><span data-stu-id="0cc9a-104">Connection-Oriented Contexts</span></span>

<span data-ttu-id="0cc9a-105">Com um [*contexto*](/windows/desktop/SecGloss/c-gly)orientado a conexão, o chamador da função é responsável por formatar mensagens.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-105">With a connection-oriented [*context*](/windows/desktop/SecGloss/c-gly), the function's caller is responsible for formatting messages.</span></span> <span data-ttu-id="0cc9a-106">O chamador depende do pacote de [*segurança*](/windows/desktop/SecGloss/s-gly) para autenticar conexões e garantir a integridade de partes específicas da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-106">The caller relies on the [*security package*](/windows/desktop/SecGloss/s-gly) to authenticate connections and to ensure the integrity of specific parts of the message.</span></span>

<span data-ttu-id="0cc9a-107">A maioria das opções de contexto está disponível para contextos orientados a conexão.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-107">Most context options are available to connection-oriented contexts.</span></span> <span data-ttu-id="0cc9a-108">Essas opções incluem autenticação mútua, detecção de reprodução e detecção de sequência, conforme descrito em [requisitos de contexto](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0cc9a-108">These options include mutual authentication, replay detection, and sequence detection, as described in [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="0cc9a-109">Um pacote de segurança define o \_ sinalizador de conexão do sinalizador SECPKG \_ para indicar que ele oferece suporte à semântica orientada por conexão.</span><span class="sxs-lookup"><span data-stu-id="0cc9a-109">A security package sets the SECPKG\_FLAG\_CONNECTION flag to indicate that it supports connection-oriented semantics.</span></span>

 

 
