---
title: Configuração do registro de aquisição silenciosa
description: Configuração do registro de aquisição silenciosa
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781446"
---
# <a name="silent-acquisition-registry-setting"></a>Configuração do registro de aquisição silenciosa

O Microsoft Windows Media Player usa o seguinte valor de registro para determinar se a aquisição silenciosa deve ser habilitada, um estado no qual o Player baixa direitos de uso automaticamente quando o usuário toca ou sincroniza o conteúdo protegido.

**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **preferências do Microsoft** \\ **MediaPlayer** \\  \\ **SilentAcquisition**

O valor de SilentAcquisition tem o seguinte formato:



| Nome              | Tipo           | Descrição                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | Defina esse valor como 1 para habilitar a aquisição silenciosa ou defina-a como 0 para desabilitar a aquisição silenciosa. O padrão é 1. |



 

Para especificar um valor, o usuário pode iniciar o Windows Media Player, abrir a caixa de diálogo **Opções** , clicar na guia **privacidade** e, em seguida, marcar ou desmarcar a caixa de seleção **baixar direitos de uso automaticamente quando eu reproduzir ou sincronizar um arquivo** . Marcar essa caixa de seleção define SilentAcquisition como 1; desmarcar a caixa de seleção o define como 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro**](registry-settings.md)
</dt> </dl>

 

 




