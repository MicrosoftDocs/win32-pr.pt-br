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
# <a name="connection-oriented-contexts"></a>Contextos de Connection-Oriented

Com um [*contexto*](/windows/desktop/SecGloss/c-gly)orientado a conexão, o chamador da função é responsável por formatar mensagens. O chamador depende do pacote de [*segurança*](/windows/desktop/SecGloss/s-gly) para autenticar conexões e garantir a integridade de partes específicas da mensagem.

A maioria das opções de contexto está disponível para contextos orientados a conexão. Essas opções incluem autenticação mútua, detecção de reprodução e detecção de sequência, conforme descrito em [requisitos de contexto](context-requirements.md).

Um pacote de segurança define o \_ sinalizador de conexão do sinalizador SECPKG \_ para indicar que ele oferece suporte à semântica orientada por conexão.

 

 
