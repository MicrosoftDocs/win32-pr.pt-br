---
description: A API de distribuição de pares define os seguintes tipos de dados.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipos de dados da API de distribuição de pares (PeerDist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753245"
---
# <a name="peer-distribution-api-data-types"></a>Tipos de dados da API de distribuição de pares

A API de distribuição de pares define os seguintes tipos de dados.


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| Tipo de dados                                                                                                                     | Descrição                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_identificador de instância PEERDIST \_**          | Um identificador associado à instância de distribuição de pares. Esse identificador é criado por [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)e usado na maioria das operações de distribuição de pares.<br/>                                          |
| <span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_identificador de conteúdo PEERDIST \_**             | Um identificador associado ao conteúdo. Esse identificador é criado por [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) e é referenciado ao abrir, fechar, adicionar ou publicar conteúdo.<br/>                     |
| <span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_identificador CONTENTINFO \_ PEERDIST** | Um identificador associado às informações de conteúdo. Esse identificador é criado por [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)e é usado ao recuperar informações de conteúdo codificado.<br/> |
| <span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_identificador de fluxo PEERDIST \_**                | Um identificador associado a um fluxo de dados. Esse identificador é criado por [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) e é referenciado durante a publicação, o fechamento ou a adição ao conteúdo transmitido.<br/>        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 7 Professional\]<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>PeerDist. h</dt> </dl> |



 

 




