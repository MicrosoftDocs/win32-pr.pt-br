---
description: Os serviços de certificados dão suporte a solicitações de certificado com base no \# formato PKCS 10 e no formato keygen (Netscape). Os serviços de certificados também dão suporte a \# solicitações de renovação PKCS 7 e a solicitações de CMS (sintaxe de mensagem criptografada).
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Requests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7870e09d930fb06d50f0cc8acfff1270db1c92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800075"
---
# <a name="requests"></a>Requests

Os serviços de certificados dão suporte a [*solicitações de certificado*](../secgloss/c-gly.md) com base no \# formato PKCS 10 e no formato keygen (Netscape). Os serviços de certificados também dão suporte a \# solicitações de renovação PKCS 7 e a solicitações de CMS (sintaxe de mensagem criptografada).

Os serviços de certificados também fornecem uma interface [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) , que contém métodos para enviar uma solicitação de certificado e (se a solicitação for aprovada) para receber o certificado emitido resultante.

As interfaces adicionais relacionadas à segurança estão disponíveis no [controle de registro de certificado](certificate-enrollment-control.md).

 

 
