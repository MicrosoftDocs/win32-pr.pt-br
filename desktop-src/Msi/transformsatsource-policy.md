---
description: Se essa política do sistema por usuário estiver definida como &\# 0034; 1&\# 0034;; o instalador pesquisará arquivos de transformação na raiz de qualquer fonte de rede na lista de origem do produto. Por padrão, as transformações são armazenadas na pasta de dados do aplicativo do perfil de um usuário.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Política de TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089850"
---
# <a name="transformsatsource-policy"></a>Política de TransformsAtSource

Se essa [política do sistema](system-policy.md) por usuário estiver definida como "1"; o instalador pesquisa arquivos de transformação na raiz de qualquer fonte de rede na lista de origem do produto. Por padrão, as transformações são armazenadas na pasta de dados do aplicativo do perfil de um usuário.

Windows Installer interpreta a política TransformsAtSource para ser a mesma que a [política TransformsSecure](transformssecure-policy.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ sz**

 

 



