---
description: HKLM \\ software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7b86a726af95e7ec9fb764d5e752057a24b3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164000"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Tipo de dados  | Intervalo                     | Valor padrão |
|------------|---------------------------|---------------|
| REG \_ DWORD | 0 (desabilitar) ou 1 (habilitar) | 0             |



 

## <a name="description"></a>Descrição

Habilita o programa de aperfeiçoamento da experiência do usuário do Windows.

## <a name="change-method"></a>Alterar Método

Para alterar o valor dessa entrada, no painel de controle, selecione **sistema e manutenção**, seguido por **relatórios de problemas e soluções**. Clique em **configurações de aperfeiçoamento da experiência do usuário** na seção Consulte também.

## <a name="activation-method"></a>Método de ativação

As alterações feitas nessa entrada entram em vigor imediatamente. A habilitação dessa chave do registro faz com que a Programa de Aperfeiçoamento da Experiência do Usuário do Windows seja habilitada para todo o computador. Desabilitar essa chave do registro faz com que o Programa de Aperfeiçoamento da Experiência do Usuário do Windows seja desabilitado para todo o computador.

Essa entrada pode ser substituída por uma configuração de Política de Grupo em sistemas que dão suporte a Política de Grupo. Enquanto a configuração Habilitar Política de Grupo do Windows Programa de Aperfeiçoamento da Experiência do Usuário CEIP está habilitada, o sistema ignora essa entrada. A configuração dessa configuração de política é armazenada na seção **políticas** em **HKLM \\ software \\ Policies \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



