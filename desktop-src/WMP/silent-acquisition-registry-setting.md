---
title: Configuração do Registro de Aquisição Silenciosa
description: Configuração do Registro de Aquisição Silenciosa
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bdab93c58dd92b5f0522f26ea192150cad4a44ae9a6edfbd0bde770f07a0262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507956"
---
# <a name="silent-acquisition-registry-setting"></a>Configuração do Registro de Aquisição Silenciosa

O Microsoft Windows Media Player usa o seguinte valor do Registro para determinar se a aquisição silenciosa deve ser habilitada, um estado no qual o player baixa direitos de uso automaticamente quando o usuário reproduz ou sincroniza o conteúdo protegido.

**HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Preferências** do Microsoft \\ **MediaPlayer** \\  \\ **SilentAcquisition**

O valor SilentAcquisition tem o seguinte formato:



| Nome              | Tipo           | Descrição                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | De definir esse valor como 1 para habilitar a aquisição silenciosa ou defini-lo como 0 para desabilitar a aquisição silenciosa. O padrão é 1. |



 

Para especificar um valor, o usuário pode iniciar o Windows Media Player,  abrir a caixa de diálogo  Opções, clicar na guia Privacidade e, em seguida, marcar ou descrevar a caixa de seleção Baixar direitos de uso automaticamente quando eu reproduzir ou sincronizar um arquivo.  A seleção dessa caixa de seleção define SilentAcquisition como 1; desempurar a caixa de seleção define-a como 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> </dl>

 

 




