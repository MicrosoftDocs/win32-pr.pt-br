---
description: Usando extensões de Shell para implementar um manipulador de vínculo de cópia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Como criar manipuladores de cabo de cópia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169433"
---
# <a name="how-to-create-copy-hook-handlers"></a>Como criar manipuladores de cabo de cópia

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md). Este documento se concentra nesses aspectos da implementação que são específicos para os manipuladores de cabo de cópia.

-   [Implementando manipuladores do cabo de cópia](#step-1-implementing-copy-hook-handlers)
-   [Registrando manipuladores de cabo de cópia](#step-2-registering-copy-hook-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-copy-hook-handlers"></a>Etapa 1: implementando manipuladores de cabo de cópia

Como todos os manipuladores de extensão de Shell, os manipuladores de cabo de cópia são objetos COM (Component Object Model) em processo implementados como DLLs. Eles exportam uma interface além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)). O Shell Inicializa o manipulador diretamente, portanto, não há necessidade de uma interface de inicialização, como [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).

A interface [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) tem um único método, [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)). Quando uma pasta está prestes a ser movida, o Shell chama esse método. Ele passa uma variedade de informações, incluindo:

-   O nome da pasta.
-   O destino da pasta ou o novo nome.
-   A operação que está sendo tentada.
-   Os atributos das pastas de origem e de destino.
-   Um identificador de janela que pode ser usado para exibir uma interface do usuário.

Quando o método [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) do manipulador é chamado, ele retorna um dos três valores a seguir para indicar ao shell como ele deve continuar.



| Valor    | Descrição                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | Permite a operação.                                                                                                                            |
| IDNO     | Impede a operação nesta pasta. O Shell pode continuar com todas as outras operações que foram aprovadas, como uma operação de cópia em lote. |
| IDCANCEL | Impede a operação atual e cancela as operações pendentes.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Etapa 2: Registrando manipuladores de gancho de cópia

Copiar manipuladores de gancho para pastas são registrados na subchave **HKEY \_ classes \_ raiz** \\ **Directory** \\ **shellex** \\ **CopyHookHandlers** . Crie uma subchave de **CopyHookHandlers** chamada para o manipulador e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador.

O exemplo a seguir adiciona a subchave **MyCopyHandler** à lista de manipuladores de cabo de cópia do Shell.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

Copiar manipuladores de gancho para objetos de impressora são registrados essencialmente da mesma maneira. A única diferença é que você deve registrá-los na subchave **HKEY \_ classes \_ root** \\ **prints** .

## <a name="remarks"></a>Comentários

Normalmente, os usuários e os aplicativos podem copiar, mover, excluir ou renomear pastas com poucas restrições. Ao implementar um manipulador de cópia de cabo, você pode controlar se essas operações ocorrem. Por exemplo, a implementação desse manipulador permite impedir que pastas críticas sejam renomeadas ou excluídas. Os manipuladores de cabo de cópia também podem ser implementados para objetos de impressora.

Os manipuladores de cabo de cópia são globais. O Shell chama todos os manipuladores registrados toda vez que um aplicativo ou um usuário tenta copiar, mover, excluir ou renomear uma pasta ou um objeto de impressora. O manipulador não executa a própria operação. Ele apenas aprova ou veta. Se todos os manipuladores aprovarem, o Shell fará a operação. Se qualquer manipulador vetar a operação, ele será cancelado e os manipuladores restantes não serão chamados. Os manipuladores de cabo de cópia não são informados sobre o êxito ou a falha da operação, portanto, eles não podem ser usados para monitorar operações de arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criar Manipuladores de Extensão de Shell](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
