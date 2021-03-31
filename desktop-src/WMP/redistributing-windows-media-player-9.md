---
title: Redistribuindo o Windows Media Player 9 Series
description: Redistribuindo o Windows Media Player 9 Series
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006061"
---
# <a name="redistributing-windows-media-player-9-series"></a>Redistribuindo o Windows Media Player 9 Series

Você pode instalar o Windows Media Player 9 Series no Windows XP usando um dos programas de instalação a seguir.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe é um superconjunto do programa de instalação do MPSetupXP.exe. Ele contém arquivos que são necessários para sistemas operacionais lançados antes do Windows XP. MPSetup.exe é funcionalmente equivalente a MPSetupXP.exe quando executado no Windows XP, mas o tamanho do arquivo do programa de instalação é maior porque não foi otimizado para instalação em sistemas operacionais Windows XP.

 

Você pode instalar o Windows Media Player 9 Series no Windows 98 Second Edition, no Windows Millennium Edition ou no Windows 2000 usando o seguinte programa de instalação.

-   MPSetup.exe

Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e nenhum prompt de reinicialização ou reinicialização.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> O parâmetro/P: \# e especifica que o pacote de instalação do Windows Media Player deve ser armazenado em cache durante a instalação do Windows Media Player. Esse comando é usado para lidar com atualizações futuras do sistema operacional. Esse comando deve ser omitido somente por administradores de ti corporativos. O único caso em que/P: \# e não deve ser incluído na linha de comando é quando você possui o sistema de destino e sabe que o sistema de destino nunca será atualizado para um sistema operacional posterior. Por exemplo, se você estiver instalando o Windows Media Player 9 Series no Windows 2000 e o computador puder ser atualizado para o Windows XP, você deverá usar/P: \# e na linha de comando. Caso contrário, após a instalação do Windows XP, os arquivos do Windows Media Player serão substituídos pelos arquivos do Windows Media Player para Windows XP.

 

A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação do Windows Media Player 9 Series.



| Parâmetro              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir a migração da biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Crie um ponto de restauração do sistema aninhado. Use esta se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto de restauração do Windows Media Player no ponto de restauração do aplicativo.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Não permitir a criação de um ponto de restauração do sistema. Esse sinalizador desabilitará a criação de um ponto de restauração do sistema. Na maioria das circunstâncias, esse sinalizador não deve ser usado para a redistribuição de software geral. Isso deve ser usado somente quando você pode fazer uma escolha explícita em nome do usuário final para não oferecer suporte à reversão dos arquivos do Windows Media Player para uma versão anterior do Player. Esse sinalizador deve ser usado somente para a implantação corporativa ou para a instalação do OEM (fabricante original do equipamento). |



 

## <a name="notes"></a>Observações

-   Os parâmetros de linha de comando diferenciam maiúsculas de minúsculas.
-   Ao suprimir o prompt de reinicialização, você deve verificar a chave do registro InstallResult e tratar a notificação de reinicialização no aplicativo de instalação de chamada.
-   O Windows Media Player 9 Series também instala o tempo de execução do Windows Media Format, portanto, não é necessário incluir o pacote de distribuição do Windows Media Player e o pacote de distribuição do Windows Media Format no mesmo pacote de redistribuição de software. Portanto, se você incluir MPSetup.exe ou MPSetupXP.exe em sua instalação, não será necessário incluir WMFdist.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo o software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




