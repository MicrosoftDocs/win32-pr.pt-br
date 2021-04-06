---
title: Alguns painéis de entrada de software do IME do leste asiático agora enviam vKey
description: Alguns painéis de entrada de software do IME do leste asiático agora enviam vKey
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823066"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a>Alguns painéis de entrada de software do IME do leste asiático agora enviam vKey

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

No Windows 8, se um dos IMEs do leste asiático for selecionado, pressionar uma chave do painel de entrada do software não enviou vKeys.

No Windows 8.1, os vKeys são enviados para as seguintes configurações:



| Idioma            | IME                                 | Windows Store | Área de trabalho |
|---------------------|-------------------------------------|---------------|---------|
| Chinês simplificado  | Microsoft Pinyin, Microsoft Wubi    | Sim           | Sim     |
| Chinês tradicional | Microsoft Changlie, Microsoft Quick | Sim           | Sim     |
| Chinês tradicional | Microsoft bopomofo                  | Não            | Não      |
| Coreano              | Microsoft IME                       | Sim           | Não      |
| Japonês            | Microsoft IME                       | Não            | Não      |



 

## <a name="manifestations"></a>Manifestações

Se o usuário escolher um IME que não envia vKeys, as funções disparadas por vKey não funcionarão.

## <a name="solution"></a>Solução

Os aplicativos que não usam uma das configurações do IME acima devem ser projetados para que os usuários possam concluir a tarefa desejada sem usar funções que exijam vKeys.

Se o usuário escolher um IME que envia vKeys, mas o aplicativo foi projetado sem essa expectativa, o aplicativo deverá ser alterado para reconhecer qual versão do Windows está em execução e responder de forma adequada.

 

 




