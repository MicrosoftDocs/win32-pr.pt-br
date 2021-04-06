---
title: contêineres e servidores
description: contêineres e servidores
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823012"
---
# <a name="containers-and-servers"></a>contêineres e servidores

Os aplicativos de documentos compostos são de dois tipos básicos: aplicativos de contêiner e aplicativos de servidor. Os aplicativos de contêiner OLE fornecem aos usuários a capacidade de criar, editar, salvar e recuperar documentos compostos. Os aplicativos de servidor OLE fornecem aos usuários meios para criar documentos e outras representações de dados que podem ser contidas como links ou incorporações em aplicativos de contêiner. Um aplicativo OLE pode ser um aplicativo de contêiner, um aplicativo de servidor ou ambos.

Os aplicativos de servidor OLE também diferem se eles são implementados como *servidores em processo* ou *servidores locais*. Um servidor em processo é uma DLL (biblioteca de vínculo dinâmico) que é executada no espaço de processo do aplicativo de contêiner. Você pode executar um servidor em processo somente de dentro do aplicativo de contêiner.

> [!Note]  
> Versões futuras do OLE habilitarão a vinculação e a inserção nos limites do computador, de modo que um aplicativo de contêiner em um computador poderá usar um objeto de documento composto fornecido por um *servidor remoto* em execução em outro computador. Do ponto de vista de um aplicativo de contêiner, qualquer aplicativo de servidor OLE executado em seu próprio espaço de processo, seja no mesmo computador ou em um computador remoto, é um *servidor processÂ*.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> <dt>

[Servidores em processo](in-process-servers.md)
</dt> </dl>

 

 




