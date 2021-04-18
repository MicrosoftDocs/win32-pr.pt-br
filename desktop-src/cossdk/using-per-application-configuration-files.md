---
description: Usando arquivos de configuração Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Usando arquivos de configuração Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784977"
---
# <a name="using-per-application-configuration-files"></a>Usando arquivos de configuração Per-Application

O uso de arquivos de configuração do COM+ por aplicativo requer as seguintes etapas básicas:

-   Configure um diretório raiz do aplicativo para um aplicativo COM+.
-   Crie aplicativos. manifest e application.config arquivos no diretório raiz do aplicativo COM+.

> [!Note]  
> Arquivos de configuração por aplicativo só estão disponíveis a partir do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.

 

**Para usar um arquivo de configuração por aplicativo**

1.  Crie uma biblioteca de classes .NET, com uma referência ao assembly System. EnterpriseServices.

2.  A biblioteca de classes deve conter o seguinte código:

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    Observe que "ConfigData1" é um exemplo de nome de configuração. Você pode substituir isso pelo nome da configuração de sua escolha.

3.  Crie um aplicativo COM+ vazio. Para obter instruções sobre como fazer isso, consulte [criando um novo aplicativo com+](creating-a-new-com--application.md).
4.  Instale a biblioteca de classes que você criou no aplicativo COM+. Para obter instruções sobre como fazer isso, consulte [instalando novos componentes](installing-new-components.md).
5.  Na ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo COM+ que você criou e selecione **Propriedades**.
6.  Na caixa de diálogo **Propriedades** , selecione a guia **ativação** .
7.  Verifique se o **tipo de ativação** está definido como **aplicativo de servidor**.
8.  Na caixa de texto **diretório raiz do aplicativo** , insira o caminho ou navegue até o diretório no qual você deseja armazenar os arquivos de configuração do aplicativo para este aplicativo.
9.  Clique em **OK**.

    Observe que você também pode especificar o diretório raiz do aplicativo COM+ por meio da Propriedade ApplicationDirectory da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) . Para obter mais informações, consulte [**aplicativos**](applications.md).

10. No diretório que você escolheu para armazenar os arquivos de configuração do aplicativo, crie um arquivo chamado *Application*. manifest. Com um editor de texto, adicione o seguinte texto a este arquivo:

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. No mesmo diretório, crie um arquivo chamado *Application*. config. Com um editor de texto, adicione o seguinte texto a este arquivo:

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    Observe que esse arquivo de configuração é apenas um exemplo. Você pode criar várias chaves com nomes e valores diferentes. No entanto, observe que "ConfigData1" corresponde ao nome da configuração usado na biblioteca de classes criada anteriormente.

12. Crie um aplicativo de console .NET, com uma referência à biblioteca de classes .NET criada anteriormente e uma referência ao assembly System. EnterpriseServices.
13. O aplicativo de console deve conter o seguinte código:
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

Execute o aplicativo de console. A saída deverá ser como a seguinte:

``` syntax
Configuration Data Number 1
```

 

 



