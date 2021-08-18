---
description: O controle WMI é um snap-in do MMC localizado no painel de controle e é usado para definir manualmente a segurança do namespace do WMI em um computador local. Você também pode definir o namespace padrão para scripts.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Definindo a segurança do namespace com o controle WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97971e09897f8fa744f72d5ad0da59dc2292ebe7ceb88f6500e3c30e124db0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992346"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Definindo a segurança do namespace com o controle WMI

O controle WMI é um snap-in do MMC localizado no **painel de controle** e é usado para definir manualmente a segurança do namespace do WMI em um computador local. Você também pode definir o namespace padrão para scripts.


O procedimento a seguir descreve como localizar o controle WMI.

**Para localizar o controle WMI**

1.  No **painel de controle**, clique duas vezes em **Ferramentas administrativas**.
2.  Na janela **Ferramentas Administrativas**, clique duas vezes em **Gerenciamento de Computador**.
3.  Na janela **Gerenciamento do computador** , expanda a árvore **serviços e aplicativos** e clique duas vezes no **controle WMI**.
4.  Clique com o botão direito do mouse no ícone **controle WMI** e selecione **Propriedades**.

O procedimento a seguir descreve como usar o controle WMI para configurar a segurança de um namespace como um modelo e, em seguida, obter as configurações de segurança programaticamente para definir a segurança para outros namespaces.

**Para definir a segurança do namespace com o controle WMI**

1.  Crie um novo namespace usando o código formato MOF (MOF).
2.  Execute o controle WMI para definir a segurança no novo namespace. No menu **Iniciar** , clique em **executar** e digite **wmimgmt. msc** ou consulte [localizando o controle WMI](#).
3.  No painel **controle WMI** , clique com o botão direito do mouse em **controle WMI**, escolha **Propriedades** e, em seguida, selecione a guia **segurança** .
4.  Navegue até o novo namespace, clique em **segurança** e, em seguida, configure grupos e permissões para o namespace.

você também pode usar Instrumentação de Gerenciamento do Windows Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) para definir a segurança do namespace. Para obter mais informações, consulte [**WMIC**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Definindo o namespace padrão para scripts

Se um script não se conectar explicitamente a um namespace ao se conectar ao WMI, o WMI usará o namespace padrão especificado nesse controle. O padrão também é encontrado na entrada do registro da seguinte maneira:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Como o namespace padrão é fácil de alterar, com esse controle ou programaticamente chamando métodos de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), especifique o namespace ao se conectar ao WMI por meio do [moniker](constructing-a-moniker-string.md) ou chamadas para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md)

**Para definir o namespace padrão para scripts**

1.  Na janela **Propriedades do controle WMI** , escolha a guia **avançado** .
2.  Clique no botão **alterar** e selecione o namespace para tornar o padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo descritores de segurança de namespace](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
