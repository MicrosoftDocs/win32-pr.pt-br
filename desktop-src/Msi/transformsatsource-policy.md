---
description: Se essa política de sistema por usuário estiver definida como &\# 0034;1&0034;; o instalador pesquisa arquivos de transformação na raiz de quaisquer fontes de rede na lista de origem do \# produto. Por padrão, as transformação são armazenadas na pasta Dados do Aplicativo do perfil de um usuário.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: TransformsAtSource Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab909fd728ce1cebba894dd8598879fa055ce762ed027cd8842cc7236a0f24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623475"
---
# <a name="transformsatsource-policy"></a>TransformsAtSource Policy

Se essa política de sistema [por usuário](system-policy.md) estiver definida como "1"; o instalador procura arquivos de transformação na raiz de quaisquer fontes de rede na lista de origem do produto. Por padrão, as transformação são armazenadas na pasta Dados do Aplicativo do perfil de um usuário.

Windows O instalador interpreta a política TransformsAtSource como a mesma que a [política TransformsSecure](transformssecure-policy.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Atual \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ SZ**

 

 



