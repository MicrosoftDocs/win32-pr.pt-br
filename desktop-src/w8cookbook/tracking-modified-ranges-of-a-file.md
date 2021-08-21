---
title: Acompanhamento de intervalos modificados de um arquivo
description: Acompanhamento de intervalos modificados de um arquivo
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
# <a name="tracking-modified-ranges-of-a-file"></a>Acompanhamento de intervalos modificados de um arquivo

## <a name="platforms"></a>Plataformas

**Clientes – Windows 8.1** (todos os SKUs)  
**Servidores – Windows Server 2012** R2  

## <a name="description"></a>Descrição

A equipe do NTFS (Sistema de Arquivos NT) adicionou um novo recurso ao Windows. O UsN Journal fará a saída de um registro USN (número de sequência de atualização) contendo intervalos modificados para um arquivo após o fechamento. Um novo tipo de registro, USN \_ RECORD \_ V4, foi introduzido para registrar esses intervalos alterados de um arquivo.

O recurso não está habilitado por padrão; os usuários devem invocar um comando FSCTL (controle do sistema de arquivos) para habilita-lo. No entanto, como outros Windows componentes podem ativar o acompanhamento de intervalo, os usuários e desenvolvedores podem perceber que o recurso está sempre habilitado. Windows permitirá que os desenvolvedores consultem o diário usn para descobrir se o controle de intervalo está habilitado.

A documentação do MSDN será fornecida posteriormente para instruir os desenvolvedores sobre como acessar registros USN \_ RECORD \_ V4.

## <a name="manifestation"></a>Manifestação

Todos os aplicativos existentes que usam o UsN Journal continuarão a funcionar bem sem problemas de compatibilidade.

 

 




