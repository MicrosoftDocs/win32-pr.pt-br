---
description: Os manipuladores de sobreposição de ícone são objetos COM (Component Object Model) em processo, implementados como DLLs.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Como implementar manipuladores de sobreposição de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22c1057f65c50b31c6627846ec77103827a0283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967896"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Como implementar manipuladores de sobreposição de ícone

Os manipuladores de sobreposição de ícone são objetos COM (Component Object Model) em processo, implementados como DLLs. Eles exportam uma interface além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Essa interface tem três métodos: [**IShellIconOverlayIdentifier:: GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**IShellIconOverlayIdentifier:: getanteriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)e [**IShellIconOverlayIdentifier:: IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-getoverlayinfo"></a>Etapa 1: implementando GetOverlayInfo

O método [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) é chamado pela primeira vez durante a inicialização. O método retorna o caminho totalmente qualificado do arquivo que contém a imagem de sobreposição de ícone e seu índice de base zero dentro do arquivo. O Shell, em seguida, adiciona a imagem à lista de imagens do sistema. As sobreposições de ícone podem estar contidas em qualquer um dos tipos de arquivo padrão, incluindo. exe,. dll e. ico.

Após a conclusão da inicialização, o Shell chama [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) quando precisa exibir a sobreposição de ícone do manipulador. O método deve retornar o mesmo nome de arquivo e índice que ele fez durante a inicialização. Embora o shell use a imagem armazenada em cache na lista de imagens do sistema em vez de carregar a imagem do arquivo, uma sobreposição de ícone ainda é identificada por seu nome de arquivo e índice.

### <a name="step-2-implementing-getpriority"></a>Etapa 2: implementando getanteriority

O método [**prepriorion**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) é chamado somente durante a inicialização. Ele atribui um valor de prioridade à sobreposição de ícone do manipulador. O valor pode variar de zero a 100, em que 100 é a prioridade mais baixa. A finalidade desse valor de prioridade é ajudar o Shell a resolver o conflito que surge quando várias sobreposições de ícone são especificadas para um único objeto. O Shell primeiro usa um conjunto interno de regras para determinar a sobreposição de ícone de prioridade mais alta. Se essas regras não resolverem o conflito, os valores atribuídos às sobreposições de ícone por **Getanteriority** determinam a prioridade.

O valor de Priority definido por [**Getanteriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) não é uma maneira confiável de resolver conflitos entre manipuladores de sobreposição de ícone não relacionados. Não há como o seu manipulador determinar quais valores de prioridade outros manipuladores estão usando. Normalmente, você deve definir o valor como zero. No entanto, o valor de prioridade é útil quando você implementa dois ou mais manipuladores de sobreposição de ícone que podem solicitar ícones de sobreposição de ícone para o mesmo objeto. Ao definir os valores de prioridade adequadamente, você pode especificar qual das sobreposições de ícone solicitadas será exibida.

### <a name="step-3-implementing-ismemberof"></a>Etapa 3: implementando IsMemberOf

O Shell chama o método [**IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) para determinar se ele deve exibir a sobreposição de ícone de um manipulador para um objeto específico. O shell especifica o objeto passando seu nome para o método. Se um manipulador quiser ter sua sobreposição de ícone exibida, **IsMemberOf** retornará S \_ OK. Caso contrário, retornará S \_ false.

Os manipuladores de sobreposição de ícone normalmente se destinam a trabalhar com um grupo específico de arquivos. Um exemplo típico é um [tipo de arquivo](fa-file-types.md), identificado por uma extensão de nome de arquivo específica. Um manipulador de sobreposição de ícone pode solicitar uma sobreposição de ícone para todos os arquivos do tipo de arquivo. Alguns manipuladores solicitam uma sobreposição de ícone somente se um arquivo do tipo de arquivo estiver em um estado específico. No entanto, os manipuladores de sobreposição de ícone são livres para solicitar a sobreposição de ícone para qualquer objeto que escolherem.

 

 
