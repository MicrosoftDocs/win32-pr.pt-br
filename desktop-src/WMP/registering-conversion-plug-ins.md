---
title: Registrando plug-ins de conversão
description: Registrando plug-ins de conversão
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, plug-ins de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, registrando
- registro, plug-ins de conversão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779986"
---
# <a name="registering-conversion-plug-ins"></a>Registrando plug-ins de conversão

Formatos de terceiros devem ser registrados antes que o Windows Media Player possa criar uma instância e usar o plug-in de conversão. Para registrar seu arquivo para conversão, você deve registrar a extensão de nome de arquivo associada ao seu formato.

A lista de extensões de nome de arquivo registrada é mantida como um conjunto de chaves do registro. Para obter detalhes sobre como registrar formatos de terceiros, consulte [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). A tabela a seguir lista as configurações de valor do registro para registrar um formato de terceiros para conversão usando um plug-in de conversão.



| Valor                  | Configuração                                                     |
|------------------------|-------------------------------------------------------------|
| **Runtime**            | 13                                                          |
| **Permissões**        | 8 (permissão para a biblioteca).                             |
| **ConvertPluginCLSID** | A ID de classe do plug-in de conversão, no formato de registro. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de plug-ins de conversão**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




