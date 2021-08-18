---
description: HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687e17bf5438406fb7a29b954bf8a2640fc0ea5d193ba49ae7fd7bd02f1f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956115"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Tipo de dados  | Intervalo                     | Valor padrão |
|------------|---------------------------|---------------|
| REG \_ DWORD | 0 (desabilitar) ou 1 (habilitar) | 0             |



 

## <a name="description"></a>Descrição

habilita o programa de aperfeiçoamento da experiência do usuário Windows.

## <a name="change-method"></a>Alterar Método

Para alterar o valor dessa entrada, no painel de controle, selecione **sistema e manutenção**, seguido por **relatórios de problemas e soluções**. clique em **Configurações de aperfeiçoamento da experiência do usuário** na seção consulte também.

## <a name="activation-method"></a>Método de ativação

As alterações feitas nessa entrada entram em vigor imediatamente. a habilitação dessa chave do registro faz com que o Programa de Aperfeiçoamento da Experiência do Usuário de Windows seja habilitado para todo o computador. desabilitar essa chave de registro faz com que o Programa de Aperfeiçoamento da Experiência do Usuário de Windows seja desabilitado para todo o computador.

Essa entrada pode ser substituída por uma configuração de Política de Grupo em sistemas que dão suporte a Política de Grupo. enquanto a configuração Windows Programa de Aperfeiçoamento da Experiência do Usuário CEIP habilitar Política de Grupo está habilitada, o sistema ignora essa entrada. a configuração dessa configuração de política é armazenada na seção **políticas** em **HKLM \\ Software \\ policies \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



