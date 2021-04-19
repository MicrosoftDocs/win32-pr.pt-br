---
title: Provedor de serviços de exemplo
description: Provedor de serviços de exemplo
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de provedor de serviço
- Gerenciador de Dispositivos, exemplo de provedor de serviço
- provedores de serviços, exemplos
- exemplos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800180"
---
# <a name="sample-service-provider"></a>Provedor de serviços de exemplo

O SDK do Windows Media Gerenciador de Dispositivos inclui um provedor de serviços de exemplo para você usar. Esse provedor de serviços inclui uma classe que relata cada disco rígido no computador como se ele fosse um dispositivo conectado. O único aplicativo que usará esse provedor de serviços é o aplicativo de exemplo; O Windows Explorer não verá os "dispositivos" relatados por este provedor de serviços. O exemplo de provedor de serviço é um objeto COM criado na ATL. As etapas a seguir explicam como usar o provedor de serviços de exemplo:

> [!Note]  
> O provedor de serviços de exemplo implementa muito poucos recursos e, portanto, não deve ser usado para testar aplicativos do Windows Media Gerenciador de Dispositivos. Para testar um aplicativo, use um provedor de serviços totalmente implementado.

 

-   O exemplo foi enviado com um erro de codificação que fará com que o provedor de serviços não funcione corretamente. Para corrigir esse erro, abra o arquivo MDSPEnumStorage. cpp instalado na pasta < *caminho de instalação do SDK*  > \\ WMFSDK95 \\ WMDM \\ MDSP \\ mshdsp, vá para a linha 185 e altere a seguinte linha:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Para isso:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compile o arquivo de MsHDSP.dll. Você pode fazer isso usando o NMAKE ou o Visual Studio. Consulte [compilando o provedor de serviços de exemplo usando o NMAKE](compiling-the-sample-service-provider-using-nmake.md) ou [compilando o provedor de serviços de exemplo usando o Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) para saber como compilar o aplicativo.
2.  Registre MsHDSP.dll usando regsvr32. A linha a seguir, digitada em uma janela de prompt de comando na mesma pasta que MsHDSP.dll, registrará o provedor de serviços de exemplo:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Para parar de representar um dispositivo, insira a seguinte linha no prompt de comando:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  Os dispositivos removíveis representados por essa DLL só podem ser vistos pelo aplicativo de exemplo fornecido com esse SDK. Compile o aplicativo de exemplo usando um dos métodos descritos em [aplicativo de desktop de exemplo](sample-desktop-application.md).
4.  Para depurar o provedor de serviços com o Visual Studio, abra o provedor de serviços no Visual Studio e selecione **Iniciar** no menu **depurar** . Na caixa de diálogo pop-up, navegue até o aplicativo de exemplo que você criou na etapa anterior e clique em **OK**, e o provedor de serviços começará a ser executado no modo de depuração.

    Para executar o provedor de serviços sem depuração no Visual Studio, basta registrar o msdhsp.dll e executar o aplicativo de desktop de exemplo que acompanha o SDK. O aplicativo de desktop de exemplo executa o provedor de serviços de exemplo automaticamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> </dl>

 

 




