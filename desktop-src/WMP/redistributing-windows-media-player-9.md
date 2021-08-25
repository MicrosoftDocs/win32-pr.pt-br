---
title: Redistribuindo Windows Media Player série 9
description: Redistribuindo Windows Media Player série 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418a780836c0a64a1b31b0d3c01a69841b695803f5db61b049915ec0d981f9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861676"
---
# <a name="redistributing-windows-media-player-9-series"></a>Redistribuindo Windows Media Player série 9

Você pode instalar Windows Media Player Série 9 no Windows XP usando um dos programas de instalação a seguir.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe é um superconjunto do programa MPSetupXP.exe instalação do . Ele contém arquivos que são necessários para sistemas operacionais liberados antes Windows XP. MPSetup.exe é funcionalmente equivalente ao MPSetupXP.exe quando executado no Windows XP, mas o tamanho do arquivo do programa de instalação é maior porque ele não foi otimizado para instalação em sistemas operacionais Windows XP.

 

Você pode instalar o Windows Media Player Série 9 no Windows 98 Second Edition, no Windows Millennium Edition ou no Windows 2000 usando o programa de instalação a seguir.

-   MPSetup.exe

Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e sem prompt de reinicialização ou reinicialização.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> O parâmetro /P: e especifica que o Windows Media Player de instalação deve ser armazenado em cache durante \# Windows Media Player configuração. Esse comando é usado para lidar com atualizações futuras do sistema operacional. Esse comando deve ser omitido somente por administradores de IT corporativos. O único caso em que /P: e não deve ser incluído na linha de comando é quando você possui o sistema de destino e sabe que o sistema de destino nunca será atualizado para um sistema operacional \# posterior. Por exemplo, se você estiver instalando o Windows Media Player Série 9 no Windows 2000 e o computador pode ser atualizado para o Windows XP, use /P: e na linha de \# comando. Caso contrário, após a Windows XP, os arquivos Windows Media Player serão substituídos pelos arquivos para Windows Media Player para Windows XP.

 

A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação Windows Media Player Série 9.



| Parâmetro              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir a migração de biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Crie um ponto de restauração aninhado do sistema. Use isso se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto Windows Media Player restauração dentro do ponto de restauração do aplicativo.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Não permitir a criação de um ponto de restauração do sistema. Esse sinalizador desabilitará a criação de um ponto de restauração do sistema. Na maioria das circunstâncias, esse sinalizador não deve ser usado para redistribuição geral de software. Isso deve ser usado somente quando você puder fazer uma escolha explícita em nome do usuário final para não dar suporte à reversões dos arquivos Windows Media Player para uma versão anterior do Player. Esse sinalizador deve ser usado somente para implantação corporativa ou instalação do OEM (fabricante de equipamento original). |



 

## <a name="notes"></a>Observações

-   Os parâmetros de linha de comando são sensíveis a minúsculas.
-   Ao suprimir o prompt de reinicialização, você deve verificar a chave do Registro InstallResult e manipular a notificação de reinicialização no aplicativo de configuração de chamada.
-   Windows Media Player Série 9 também instala o runtime do formato de mídia do Windows, portanto, não há necessidade de incluir o pacote de distribuição do Windows Media Player e o pacote de distribuição de runtime do formato de mídia do Windows no mesmo pacote de redistribuição de software. Portanto, se você incluir MPSetup.exe ou MPSetupXP.exe em sua instalação, não precisará incluir WMFdist.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




