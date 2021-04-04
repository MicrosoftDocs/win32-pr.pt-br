---
title: Script personalizado de RAS
description: Os desenvolvedores podem criar uma DLL de script personalizado que resida em um computador cliente RAS. Essa DLL pode se comunicar com o servidor durante o processo de estabelecimento de uma conexão.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c625f020d9dafcb352c5f1b382014f9dba189330
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917412"
---
# <a name="ras-custom-scripting"></a>Script personalizado de RAS

Os desenvolvedores podem criar uma DLL de script personalizado que resida em um computador cliente RAS. Essa DLL pode se comunicar com o servidor durante o processo de estabelecimento de uma conexão.

**Windows NT:** O script personalizado não está disponível.

## <a name="setting-up-the-dll"></a>Configurando a DLL

Para configurar a DLL, crie um valor com o nome **CustomScriptDllPath** na seguinte chave do registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Esse valor deve ser do tipo **reg \_ expande \_ sz**. O valor deve conter o caminho para a DLL de script personalizado. Somente uma DLL de script personalizado tem suporte para cada computador cliente RAS.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interação entre o servidor, o RAS e o Custom-Scripting DLL

A DLL de script personalizado deve exportar um único ponto de entrada: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). O RAS chama essa função durante o \_ estado interativo do RASCS do processo de conexão. O \_ estado interativo do RASCS é um estado de pausa, que permite ao usuário interagir com uma interface do usuário apresentada pela DLL de script personalizado. Consulte [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) para obter mais informações sobre Estados de conexão.

O RAS passará como parâmetros para a função [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) :

-   Um identificador para a porta no computador cliente que está sendo usado para a conexão.
-   Cadeias de caracteres que identificam o catálogo telefônico e a entrada para a conexão.
-   O RAS também passa um identificador para uma janela para permitir que a DLL apresente uma interface do usuário.
-   Um conjunto de ponteiros de função que a DLL pode usar para se comunicar com o servidor.

Consulte [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) para obter mais informações sobre esses parâmetros.

O RAS passa um ponteiro para uma estrutura [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) como o último parâmetro para [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Essa estrutura contém um ponteiro para uma função do tipo [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). A DLL de script personalizado chama essa função para modificar as configurações de comunicação na porta usada pela conexão.

O RAS Media a interação entre o servidor e a DLL de script personalizado. Normalmente, o servidor inicia a caixa de diálogo. Por exemplo, o servidor pode solicitar o nome de usuário e a senha do usuário.

Ao usar o script personalizado para estabelecer uma conexão, o servidor não precisa estar executando o Windows NT 4,0 ou o Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>A interface do usuário de script personalizado deve dar suporte a IDCANCEL

Se a discagem personalizada exibir uma interface do usuário, a interface do usuário deverá dar suporte a \_ mensagens de comando do WM em que LOWORD (*wParam*) seja igual a IDCANCEL.

## <a name="configuring-the-connection"></a>Configurando a conexão

O ponto de entrada [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) pode ser chamado de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) ou, no Windows XP, de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga), defina a \_ opção RASEO CustomScript na entrada do catálogo telefônico para a conexão. Consulte o membro **dwfOptions** de [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para obter uma descrição das opções de entrada de catálogo telefônico. Use as funções [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir essa opção programaticamente.

**Windows XP:** Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala), a chamada para **RasDial** deve especificar uma estrutura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) , e essa estrutura deve especificar o \_ sinalizador RDEOPT UseCustomScripting. Além disso, a entrada do catálogo telefônico para a conexão deve especificar a \_ opção RASEO CustomScript, conforme descrito no parágrafo anterior.

## <a name="invoking-the-custom-scripting-dll"></a>Invocando a DLL de script personalizado

Se o usuário ativar uma conexão para uma entrada de catálogo telefônico que tenha RASEO \_ CustomScript definido, o RAS invocará a DLL de script personalizado. Nesse cenário, o RAS invoca a DLL de script personalizado de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Para invocar a DLL de script personalizado programaticamente, estabeleça a conexão usando a função [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) . No Windows XP, a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) também invoca a DLL de script personalizado.

 

 