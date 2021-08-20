---
description: Usando extensões do Shell para implementar um manipulador de gancho de cópia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Como criar manipuladores de gancho de cópia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a20831103d26233f76f64f32d07bf50977a746669fff7e5562da159e14027d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117679085"
---
# <a name="how-to-create-copy-hook-handlers"></a>Como criar manipuladores de gancho de cópia

Os procedimentos gerais para implementar e registrar um manipulador de extensão do Shell são discutidos em Criando manipuladores de [extensão do Shell.](handlers.md) Este documento se concentra nos aspectos da implementação que são específicos para copiar manipuladores de gancho.

-   [Implementando manipuladores de gancho de cópia](#step-1-implementing-copy-hook-handlers)
-   [Registrando manipuladores de gancho de cópia](#step-2-registering-copy-hook-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-copy-hook-handlers"></a>Etapa 1: Implementando manipuladores de gancho de cópia

Como todos os manipuladores de extensão do Shell, manipuladores de gancho de cópia são objetos COM (Component Object Model em processo) implementados como DLLs. Eles exportam uma interface além de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**ICopyHook.**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) O Shell inicializa o manipulador diretamente, portanto, não há necessidade de uma interface de inicialização, como [**IShellExtInit.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

A interface [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) tem um único método, [**ICopyHook::CopyCallback.**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) Quando uma pasta está prestes a ser movida, o Shell chama esse método. Ele passa uma variedade de informações, incluindo:

-   O nome da pasta.
-   O destino ou o novo nome da pasta.
-   A operação que está sendo tentada.
-   Os atributos das pastas de origem e destino.
-   Um alça de janela que pode ser usado para exibir uma interface do usuário.

Quando o método [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) do manipulador é chamado, ele retorna um dos três valores a seguir para indicar ao Shell como ele deve continuar.



| Valor    | Descrição                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Idyes    | Permite a operação.                                                                                                                            |
| Idno     | Impede a operação nessa pasta. O Shell pode continuar com quaisquer outras operações que foram aprovadas, como uma operação de cópia em lote. |
| Idcancel | Impede a operação atual e cancela todas as operações pendentes.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Etapa 2: Registrando manipuladores de gancho de cópia

Manipuladores de gancho de cópia para pastas são registrados na **subkey HKEY \_ CLASSES \_ ROOT** \\ **Directory** \\ **shellex** \\ **CopyHookHandlers.** Crie uma sub-chave **de CopyHookHandlers** chamada para o manipulador e de definido o valor padrão da sub-chave como a forma de cadeia de caracteres do GUID do CLSID (identificador de classe) do manipulador.

O exemplo a seguir adiciona a sub-chave **MyCopyHandler** à lista do Shell de manipuladores de gancho de cópia.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

Manipuladores de gancho de cópia para objetos de impressora são registrados essencialmente da mesma maneira. A única diferença é que você deve registrá-los na **sub-chave Impressoras RAIZ HKEY \_ \_ CLASSES.** \\ 

## <a name="remarks"></a>Comentários

Normalmente, usuários e aplicativos podem copiar, mover, excluir ou renomear pastas com poucas restrições. Ao implementar um manipulador de gancho de cópia, você pode controlar se essas operações ocorrem. Por exemplo, implementar esse manipulador permite que você impeça que pastas críticas seja renomeada ou excluída. Manipuladores de gancho de cópia também podem ser implementados para objetos de impressora.

Manipuladores de gancho de cópia são globais. O Shell chama todos os manipuladores registrados sempre que um aplicativo ou usuário tenta copiar, mover, excluir ou renomear uma pasta ou objeto de impressora. O manipulador não executa a operação em si. Ele apenas o aprova ou veta. Se todos os manipuladores aprovarem, o Shell faz a operação. Se qualquer manipulador vetar a operação, ela será cancelada e os manipuladores restantes não serão chamados. Manipuladores de gancho de cópia não são informados do êxito ou da falha da operação, portanto, eles não podem ser usados para monitorar operações de arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criar Manipuladores de Extensão de Shell](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
