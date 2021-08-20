---
title: Scripts personalizados ras
description: Os desenvolvedores podem criar uma DLL de script personalizado que reside em um computador cliente RAS. Essa DLL pode se comunicar com o servidor durante o processo de estabelecer uma conexão.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ac0bd83b8d7c48ee8b0468d89a70d19a5e5e6555b9a8bc8ac86d66c8cd666e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673276"
---
# <a name="ras-custom-scripting"></a>Scripts personalizados ras

Os desenvolvedores podem criar uma DLL de script personalizado que reside em um computador cliente RAS. Essa DLL pode se comunicar com o servidor durante o processo de estabelecer uma conexão.

**Windows NT:** O script personalizado não está disponível.

## <a name="setting-up-the-dll"></a>Configurando a DLL

Para configurar a DLL, crie um valor com o nome **CustomScriptDllPath** na seguinte chave do Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Esse valor deve ser do tipo **REG \_ EXPAND \_ SZ.** O valor deve conter o caminho para a DLL de script personalizado. Há suporte apenas para uma DLL de script personalizado para cada computador cliente RAS.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interação entre o servidor, RAS e a Custom-Scripting DLL

A DLL de script personalizado deve exportar um único ponto de entrada: [**RasCustomScriptExecute.**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) RAS chama essa função durante o estado Interativo rascs \_ do processo de conexão. O estado Interativo do RASCS é um estado em pausa, que permite que o usuário interaja com uma interface do usuário apresentada pela DLL de \_ script personalizado. Consulte [**RASCONNSTATE para**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) obter mais informações sobre os estados de conexão.

RAS passará como parâmetros para a [**função RasCustomScriptExecute:**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)

-   Um handle para a porta no computador cliente que está sendo usado para a conexão.
-   Cadeias de caracteres que identificam a lista telefônica e a entrada para a conexão.
-   O RAS também passa um alça para uma janela para habilitar a DLL a apresentar uma interface do usuário.
-   Um conjunto de ponteiros de função que a DLL pode usar para se comunicar com o servidor.

Consulte [**RasCustomScriptExecute para**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) obter mais informações sobre esses parâmetros.

RAS passa um ponteiro para uma [**estrutura RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) como o último parâmetro para [**RasCustomScriptExecute.**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) Essa estrutura contém um ponteiro para uma função do tipo [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). A DLL de script personalizado chama essa função para modificar as configurações de comunicação na porta que está sendo usada pela conexão.

O RAS media a interação entre o servidor e a DLL de script personalizado. Normalmente, o servidor inicia a caixa de diálogo. Por exemplo, o servidor pode solicitar o nome de usuário e a senha do usuário.

Ao usar scripts personalizados para estabelecer uma conexão, o servidor não precisa estar executando Windows NT 4.0 ou Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>Scripts personalizados Interface do Usuário devem dar suporte a IDCANCEL

Se o discador personalizado exibir uma interface do usuário, a interface do usuário deverá dar suporte a mensagens WM COMMAND em que \_ LOWORD(*wParam*) é igual a IDCANCEL.

## <a name="configuring-the-connection"></a>Configurando a conexão

O ponto de entrada [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) pode ser invocado de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) ou, no Windows XP, de [**RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) de [**RasDialDlg,**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)defina a opção RASEO CustomScript na entrada \_ de phone-book para a conexão. Consulte o **membro dwfOptions** de [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para ver uma descrição das opções de entrada de livro de telefone. Use as [**funções RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir essa opção programaticamente.

**Windows XP:** Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala), a chamada para **RasDial** deve especificar uma estrutura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) e essa estrutura deve especificar o sinalizador VOCOPT \_ UseCustomScripting. Além disso, a entrada de phone-book para a conexão deve especificar a opção RASEO \_ CustomScript, conforme descrito no parágrafo anterior.

## <a name="invoking-the-custom-scripting-dll"></a>Invocando a DLL de script personalizado

Se o usuário ativar uma conexão para uma entrada de livro telefônica que tenha RASEO CustomScript definido, o RAS invocará a DLL de \_ script personalizado. Nesse cenário, o RAS invoca a DLL de script personalizado de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Para invocar a DLL de script personalizado programaticamente, estabeleça a conexão usando a [**função RasDialDlg.**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) No Windows XP, a [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) também invoca a DLL de script personalizado.

 

 