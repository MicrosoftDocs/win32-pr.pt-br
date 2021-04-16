---
description: 'A extensão do snap-in de anexos não tem como consultar diretamente o banco de dados de segurança para recuperar informações. Em vez disso, ele deve consultar essas informações dos snap-ins de configuração de segurança usando ISceSvcAttachmentData:: GetData.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Obtendo dados dos snap-ins de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506056"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a>Obtendo dados dos snap-ins de configuração

A extensão do snap-in de anexos não tem como consultar diretamente o banco de dados de segurança para recuperar informações. Em vez disso, ele deve consultar essas informações dos snap-ins de configuração de segurança usando [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).

O snap-in de anexo pode recuperar todos os dados quando ele é inicializado ou pode recuperar informações quando seu nó é aberto.

> [!Note]  
> Você deve usar o método [**ISceSvcAttachmentData:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) para liberar o buffer alocado pelo método de snap-in de configuração de segurança [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).

 

 

 



