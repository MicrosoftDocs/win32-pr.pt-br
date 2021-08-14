---
title: Controlando intervalos modificados de um arquivo
description: Controlando intervalos modificados de um arquivo
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6998d2706cd4d8bdb4e94b95fd0e617dbbf4e3a1b288d33dbcebe5528d544c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852023"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Controlando intervalos modificados de um arquivo

## <a name="platforms"></a>Plataformas

**clientes-** Windows 8.1 (todas as SKUs)  
**servidores-** Windows Server 2012 R2  

## <a name="description"></a>Descrição

A equipe do sistema de arquivos NT (NTFS) adicionou um novo recurso para Windows. O diário de USN produzirá um registro USN (número de sequência de atualização) contendo intervalos modificados para um arquivo após o fechamento. Um novo tipo de registro, \_ registro USN \_ v4, foi introduzido para registrar esses intervalos alterados de um arquivo.

O recurso não está habilitado por padrão; os usuários devem invocar um comando de controle do sistema de arquivos (FSCTL) para habilitá-lo. no entanto, como outros componentes de Windows podem ativar o controle de intervalo, os usuários e desenvolvedores podem perceber que o recurso está sempre habilitado. Windows permitirá que os desenvolvedores consultem o diário de USN para descobrir se o rastreamento de intervalo está habilitado.

A documentação do MSDN será fornecida em uma data posterior para instruir os desenvolvedores em como \_ acessar \_ registros v4 de registro USN.

## <a name="manifestation"></a>Manifestação

Todos os aplicativos existentes que usam o diário de USN continuarão funcionando bem sem problemas de compatibilidade.

 

 




