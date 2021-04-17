---
title: Controlando intervalos modificados de um arquivo
description: Controlando intervalos modificados de um arquivo
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105773100"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Controlando intervalos modificados de um arquivo

## <a name="platforms"></a>Plataformas

**Clientes-** Windows 8.1 (todas as SKUs)  
**Servidores-** Windows Server 2012 R2  

## <a name="description"></a>Descrição

A equipe do sistema de arquivos NT (NTFS) adicionou um novo recurso ao Windows. O diário de USN produzirá um registro USN (número de sequência de atualização) contendo intervalos modificados para um arquivo após o fechamento. Um novo tipo de registro, \_ registro USN \_ v4, foi introduzido para registrar esses intervalos alterados de um arquivo.

O recurso não está habilitado por padrão; os usuários devem invocar um comando de controle do sistema de arquivos (FSCTL) para habilitá-lo. No entanto, como outros componentes do Windows podem ativar o controle de intervalo, os usuários e desenvolvedores podem perceber que o recurso está sempre habilitado. O Windows permitirá que os desenvolvedores consultem o diário de USN para descobrir se o rastreamento de intervalo está habilitado.

A documentação do MSDN será fornecida em uma data posterior para instruir os desenvolvedores em como \_ acessar \_ registros v4 de registro USN.

## <a name="manifestation"></a>Manifestação

Todos os aplicativos existentes que usam o diário de USN continuarão funcionando bem sem problemas de compatibilidade.

 

 




