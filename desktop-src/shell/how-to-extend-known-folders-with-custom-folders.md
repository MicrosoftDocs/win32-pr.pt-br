---
description: ISVs (fornecedores independentes de software) podem estender o conjunto de pastas conhecidas em um sistema registrando suas próprias pastas conhecidas.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Como estender pastas conhecidas com pastas personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a04a5ef10c8e3ee909944e6782cf32ca6aa2aa6b50e03f018f31a6aafe529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350866"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>Como estender pastas conhecidas com pastas personalizadas

ISVs (fornecedores independentes de software) podem estender o conjunto de pastas conhecidas em um sistema registrando suas próprias pastas conhecidas. Depois de registrado, essas pastas de terceiros são conhecidas pelo sistema. Eles são encontrados por qualquer chamada para [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids). Observe que uma pasta conhecida deve ser uma pasta por computador. Não é possível criar uma pasta por usuário conhecida.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Defina sua pasta conhecida por meio de uma estrutura de [**\_ definição de KNOWNFOLDER**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .

### <a name="step-2"></a>Etapa 2:

Registre a pasta conhecida por meio de uma chamada para [**IKnownFolderManager:: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).

## <a name="remarks"></a>Comentários

Se você criar uma pasta conhecida para seu aplicativo como parte do seu procedimento de instalação, também deverá incluir [**IKnownFolderManager:: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) como parte do seu código de desinstalação.

Considere por que você deseja que sua pasta seja incluída no sistema de pastas conhecido antes de registrá-la. Você deve ter um motivo válido para elevar sua pasta para esse nível de visibilidade do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de pastas conhecidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
