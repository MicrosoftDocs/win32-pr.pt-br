---
description: Painel de controle do HKCU \\ \\ desktop.
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1ac7c0f2ee9d87911c0db195df89e2c27dcf1b19c0e9dac70d1517b0ad30ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571346"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**Painel de controle do HKCU \\ \\ Desktop**



| Tipo de dados | Intervalo       | Valor padrão |
|-----------|-------------|---------------|
| REG \_ sz   | *Nome do arquivo* | (Nenhuma)        |



 

## <a name="description"></a>Descrição

Especifica o nome do arquivo executável de proteção de tela.

## <a name="change-method"></a>Alterar Método

Para alterar o valor dessa entrada, no painel de controle, clique duas vezes em **Exibir**, clique na guia **proteção de tela** e selecione uma proteção de tela na lista **proteção de tela** .

Você também pode alterar essa entrada com a função de API (interface de programação de aplicativo) **InstallScreenSaver**, que é exportada por Desk.cpl. Você pode acessar essa função com a linha de comando **rundll32.exe desk.cpl,** o *arquivo* InstallScreenSaver, em que *File* é o nome de um arquivo executável de proteção de tela.

## <a name="activation-method"></a>Método de ativação

As alterações feitas nessa entrada entram em vigor na próxima vez em que o sistema iniciar uma proteção de tela. As alterações feitas nessa entrada enquanto uma proteção de tela está em execução não têm efeito sobre a proteção de tela em execução.

## <a name="notes"></a>Observações

-   Windows sistemas operacionais adicione essa entrada ao registro quando você usa **exibir** no painel de controle para selecionar uma proteção de tela. Se você desabilitar todas as proteções de tela escolhendo **(nenhum)** na lista proteção de tela, o sistema operacional excluirá essa entrada do registro e chamará a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com *uiAction* igual a SPI \_ SETSCREENSAVEACTIVE e *uiParam* igual a **false**.
-   Essa entrada pode ser substituída por uma configuração de Política de Grupo em sistemas que dão suporte a Política de Grupo. Enquanto a configuração Política de Grupo **nome do executável de proteção de tela** está habilitada, o sistema ignora essa entrada. A configuração dessa configuração de política é armazenada na entrada **SCRNSAVE.EXE** , que está na subchave **Policies** .

 

 
