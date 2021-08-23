---
title: O armazenamento aprimorado agora é opcional para WINPE e SKU do servidor
description: O armazenamento aprimorado agora é opcional para WINPE e SKU do servidor
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3777d4df386b071166fcfa17a60654c62e039d9137f73deaf2d85d54e2519e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028844"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>O armazenamento aprimorado agora é opcional para WINPE e SKU do servidor

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

O armazenamento aprimorado sempre estava disponível em Windows 7 dispositivos USB. Com o lançamento do Windows 8, ele está disponível para todos os dispositivos de armazenamento. Em dispositivos baseados em cliente, ele é habilitado por padrão; em dispositivos de servidor, ele é opcional e deve ser provisionado por meio Windows WinPE (Ambiente de Pré-instalação).

## <a name="manifestation"></a>Manifestação

O dispositivo de servidor falhará se o armazenamento aprimorado não estiver habilitado.

Os dispositivos de inicialização devem ser provisionados por meio do WinPE com isso habilitado.

## <a name="solution"></a>Solução

Como o armazenamento aprimorado é opcional para o servidor de runtime, os desenvolvedores devem adicioná-lo ao WinPE para provisionamento e ativação dessas unidades. Confira o guia de implantação para obter detalhes.

Os administradores de servidor devem configurar explicitamente seu servidor para usar o armazenamento aprimorado.

 

 




