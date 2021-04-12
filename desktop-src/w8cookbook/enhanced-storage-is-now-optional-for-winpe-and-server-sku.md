---
title: O armazenamento aprimorado agora é opcional para o WINPE e o SKU do servidor
description: O armazenamento aprimorado agora é opcional para o WINPE e o SKU do servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104294547"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>O armazenamento aprimorado agora é opcional para o WINPE e o SKU do servidor

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

O armazenamento aprimorado estava sempre disponível em dispositivos USB do Windows 7. Com o lançamento do Windows 8, ele está disponível para todos os dispositivos de armazenamento. Em dispositivos baseados em cliente, ele é habilitado por padrão; em dispositivos de servidor, ele é opcional e deve ser provisionado por meio de Ambiente de Pré-Instalação do Windows (WinPE).

## <a name="manifestation"></a>Manifestação

O dispositivo do servidor falhará se o armazenamento avançado não estiver habilitado.

Os dispositivos de inicialização devem ser provisionados por meio do WinPE com essa habilitação.

## <a name="solution"></a>Solução

Como o armazenamento avançado é opcional para o servidor de tempo de execução, os desenvolvedores devem adicioná-lo ao WinPE para provisionamento e ativação dessas unidades. Consulte o guia de implantação para obter detalhes.

Os administradores de servidor devem configurar explicitamente seu servidor para usar o armazenamento avançado.

 

 




