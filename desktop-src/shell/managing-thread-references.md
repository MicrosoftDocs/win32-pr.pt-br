---
description: Este artigo contém informações sobre o gerenciamento de referências de thread usando funções das funções de utilitário leve do Shell.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Gerenciando referências de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6380957f5f8ef9be62e291820fe12d715f31a5f5bb5ba81b80aa1c8606478e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968915"
---
# <a name="managing-thread-references"></a>Gerenciando referências de thread

Este artigo contém informações sobre o gerenciamento de referências de thread usando funções das funções de utilitário leve do Shell.


Situações surgem quando um thread pai deve ser mantido ativo durante o tempo de vida de um thread filho. Por exemplo, se um objeto Component Object Model (COM) for criado no thread pai e tiver marshaled para o thread filho, esse thread pai não poderá ser encerrado antes do thread filho. Para fazer isso, o Shell fornece essas funções.

-   [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Use essas funções em seu thread pai, conforme descrito aqui.

1.  Declare um procedimento de thread definido pelo aplicativo seguindo a forma da [*função ThreadProc.*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  Em seu [*ThreadProc,*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))chame [**SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) para criar uma referência ao thread. Isso fornece um ponteiro para uma instância [**de IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Esse **IUnknown usa** o valor apontado por *pcRef* para manter uma contagem de referência. Desde que essa contagem seja maior que 0, o thread permanecerá ativo.
3.  Usando esse ponteiro para [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), chame [**SHSetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) em [*seu ThreadProc.*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) Isso define a referência para que as chamadas subsequentes para [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) tenham algo a recuperar.
4.  Se o [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) criar outro thread, *o ThreadProc* desse thread poderá chamar [**SHGetThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) com o ponteiro [**para IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtido por [**SHCreateThreadRef.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) Isso incrementa a contagem de referência apontada pelo parâmetro *pcRef* em **SHCreateThreadRef**.
5.  Crie o thread. Isso geralmente é feito chamando [**SHCreateThread,**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread)passando um ponteiro para [*o ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) no *parâmetro pfnThreadProc.* Passe também o sinalizador \_ CTF THREAD \_ REF no parâmetro *dwFlags.* O thread está ativo enquanto *o ThreadProc está* em execução.
6.  Quando um thread filho é criado, passe o sinalizador **\_ REF \_ COUNTED CTF** no parâmetro *dwFlags* na chamada para [**seu SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  Conforme os threads filho são concluídos e liberados, o valor apontado pelo *pcRef* do thread pai diminui. Depois que todos os threads filho são concluídos, o [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) original pode concluir e liberar a referência de thread final, baixando a contagem de referência para 0. Nesse ponto, a referência ao thread original aberto por [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) é liberada e o thread é concluído.

Outra função relacionada é [**SHReleaseThreadRef.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref) Essa função será chamada pelo [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) se o thread tiver sido criado usando [**SHCreateThread**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) com o sinalizador **\_ CTF THREAD \_ REF.** No entanto, *o ThreadProc* não precisa fazer isso implicitamente. Chamar [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro para [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) obtido por [**meio de SHCreateThreadRef**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) é tudo o que precisa ser feito.

 

 
