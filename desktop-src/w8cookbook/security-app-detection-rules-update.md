---
title: Atualização de regras de detecção de aplicativo de segurança
description: Atualização de regras de detecção de aplicativo de segurança
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008497"
---
# <a name="security-app-detection-rules-update"></a>Atualização de regras de detecção de aplicativo de segurança

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


### <a name="description"></a>Descrição

Os aplicativos da Windows Store que estão sendo adicionados ao Windows 8 estão sendo instalados em um local comum em "arquivos de programas" (% ProgramFiles%) chamados \\ arquivos de programas \\ WindowsApps.

### <a name="manifestation"></a>Manifestação

Isso pode causar colisões com configurações existentes e alguns detectores antivírus/Antimalware veem esse local como um local potencial que é uma causa de preocupação.

### <a name="mitigation"></a>Atenuação

As recomendações atuais são:

-   Afastar-se dos \\ arquivos de programas \\ WindowsApps para armazenar aplicativos personalizados
-   Fornecedores de antivírus/Antimalware devem atualizar sua heurística para que não identifiquem esse local como um local de malware

 

 




