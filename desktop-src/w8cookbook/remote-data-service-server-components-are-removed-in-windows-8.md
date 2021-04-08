---
title: Serviço de dados remoto removido
description: Os componentes do servidor do serviço de dados remoto são removidos do Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Servidor RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103917746"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>Os componentes do servidor do serviço de dados remoto são removidos do Windows 8

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows 8  
**Servidores** -Windows Server 2012  



## <a name="description"></a>Descrição

O servidor RDS (serviço de dados remotos) não está disponível no Windows 8:

-   O arquivo msadcf.dll, que hospeda o "objeto comercial" padrão RDSServer. datafactory, é removido e seus arquivos associados (msadcfr.dll, msadcfr.dll. mui, Handler. reg e handsafe. reg) são removidos
-   O arquivo msdfmap.dll, que é o manipulador padrão, é removido e o msdfmap.ini de arquivo é removido
-   O arquivo msadcs.dll, ISAPI, é removido

## <a name="manifestation"></a>Manifestação

Os clientes não podem hospedar um servidor RDS no Windows 8.

## <a name="mitigation"></a>Atenuação

Os clientes podem manter seu servidor RDS em um computador com o Windows 7 ou outros sistemas operacionais de nível inferior.

## <a name="solution"></a>Solução

Os clientes podem manter seu servidor RDS em um computador com o Windows 7 ou outros sistemas operacionais de nível inferior.

## <a name="resources"></a>Recursos

[Roteiro de tecnologias de acesso a dados](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 