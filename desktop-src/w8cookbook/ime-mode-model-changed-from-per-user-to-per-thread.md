---
title: Alterações do modelo do modo IME
description: O modelo de modo IME mudou de por usuário para por thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443241"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>O modelo de modo IME mudou de por usuário para por thread

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

No Windows 8, o modo de conversão IME e o modo de frase IME foram baseados no contexto do usuário e a alteração do modo de um aplicativo afetou todos os outros aplicativos. Esse comportamento pode ser desabilitado usando a configuração "Deixe-me definir um método de entrada diferente para cada janela de aplicativo" na seção Configurações avançadas do painel de controle de idioma.

Para melhorar a compatibilidade, em Windows 8.1 os modos são armazenados em um contexto de entrada, independentemente de como o controle "Deixe-me definir um método de entrada diferente para cada janela do aplicativo" está definido. No Windows 8.1, a configuração "Deixe-me definir um método de entrada diferente para cada janela de aplicativo" afeta apenas a seleção do próprio método de entrada.

Na inicialização do aplicativo, o modo IME é definido com os seguintes padrões:



| &nbsp;   | Painel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Ativado                   | Desativado               |
| CHS, CHT  | Ativado                   | Ativado                |



 

## <a name="manifestations"></a>Manifestações

Quando um usuário altera o modo IME em um aplicativo, a alteração não afeta outros aplicativos.

## <a name="resources"></a>Recursos

-   [Valores do modo de conversão do IME](../intl/ime-conversion-mode-values.md)
-   [Valores do modo de frase do IME](../intl/ime-sentence-mode-values.md)

 

 