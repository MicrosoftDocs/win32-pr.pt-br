---
title: contêineres e servidores
description: contêineres e servidores
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d301d85bc317cd4e60d609e73b6b7232cfb5634a33bf32a2496fe8cd672d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993566"
---
# <a name="containers-and-servers"></a>contêineres e servidores

Os aplicativos compostos de documentos são de dois tipos básicos: aplicativos de contêiner e aplicativos de servidor. Os aplicativos de contêiner OLE fornecem aos usuários a capacidade de criar, editar, salvar e recuperar documentos compostos. Os aplicativos de servidor OLE fornecem aos usuários os meios para criar documentos e outras representações de dados que podem ser contidas como links ou incorporações em aplicativos de contêiner. Um aplicativo OLE pode ser um aplicativo de contêiner, um aplicativo de servidor ou ambos.

Os aplicativos de servidor OLE também diferem se são implementados como servidores em *processo* ou *servidores locais.* Um servidor em processo é uma DLL (biblioteca de vínculo dinâmico) que é executado no espaço de processo do aplicativo de contêiner. Você pode executar um servidor em processo somente de dentro do aplicativo de contêiner.

> [!Note]  
> Versões futuras do OLE permitirão a vinculação e *a* incorporação entre limites do computador, para que um aplicativo de contêiner em um computador possa usar um objeto de documento composto fornecido por um servidor remoto em execução em outro computador. Do ponto de vista de um aplicativo de contêiner, qualquer aplicativo de servidor OLE executado em seu próprio espaço de processo, seja no mesmo computador ou em um computador remoto, é um servidor fora de *processo.*

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> <dt>

[Servidores em processo](in-process-servers.md)
</dt> </dl>

 

 




