---
description: O WMI registra automaticamente a DLL do provedor de exibição durante o processo de instalação do WMI. No entanto, você ainda precisa registrar o provedor de exibição com WMI para cada namespace que conterá classes de exibição.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrando o provedor de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a119816d388e07f1f032557af1171bb2666ef02a63d959b843b99b7942a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992456"
---
# <a name="registering-the-view-provider"></a>Registrando o provedor de exibição

O WMI registra automaticamente a DLL do provedor de exibição durante o processo de instalação do WMI. No entanto, você ainda precisa registrar o provedor de exibição com WMI para cada namespace que conterá classes de exibição.

O procedimento a seguir descreve como registrar o provedor de exibição.

**Para registrar o provedor de exibição**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) para descrever a implementação do provedor de exibição.

    A instância do [**\_ \_ Win32Provider**](--win32provider.md) descreve o nome do provedor e seu identificador de classe (CLSID), bem como as configurações de segurança padrão.

    O exemplo de código a seguir descreve uma implementação do [**\_ \_ Win32Provider**](--win32provider.md).

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  Crie uma instância da classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

    O exemplo de código a seguir mostra como criar uma instância da classe **\_ \_ InstanceProviderRegistration** .

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  Crie uma instância da classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) se desejar ter os métodos de suporte da classe de exibição Union.

    O exemplo de código a seguir mostra como criar uma instância da classe **\_ \_ MethodProviderRegistration** .

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Compile seu código MOF usando o compilador MOF ([Mofcomp](mofcomp.md)) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Se você salvar o exemplo de código MOF listado anteriormente em um arquivo chamado Viewtest. MOF, use o comando Mofcomp para carregar o código MOF no namespace de destino. *NamespacePath* é o namespace no qual você deseja criar a instância da classe View.

    Digite o seguinte comando em um prompt de comando para carregar o código MOF no namespace de destino.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).

 

 



