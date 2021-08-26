---
title: Provedor de Serviços de Exemplo
description: Provedor de Serviços de Exemplo
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Mídia Gerenciador de Dispositivos, exemplos
- Gerenciador de Dispositivos,exemplos
- Windows Exemplo Gerenciador de Dispositivos de provedor de serviços
- Gerenciador de Dispositivos, exemplo de provedor de serviços
- provedores de serviços, exemplos
- exemplos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eead5296a1ba3213f291027c0b1e4d50275497ad2ebe5a3feaea994e4a5c8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004906"
---
# <a name="sample-service-provider"></a>Provedor de Serviços de Exemplo

O Windows De mídia Gerenciador de Dispositivos SDK inclui um provedor de serviços de exemplo para você usar. Esse provedor de serviços inclui uma classe que relata cada disco rígido no computador como se fosse um dispositivo anexado. O único aplicativo que usará esse provedor de serviços é o aplicativo de exemplo; Windows O Explorer não verá os "dispositivos" relatados por esse provedor de serviços. O exemplo do provedor de serviços é um objeto COM criado na ATL. As etapas a seguir explicam como usar o provedor de serviços de exemplo:

> [!Note]  
> O provedor de serviços de exemplo implementa poucos recursos e, portanto, não deve ser usado para testar Windows de Gerenciador de Dispositivos mídia. Para testar um aplicativo, use um provedor de serviços totalmente implementado.

 

-   O exemplo foi enviado com um erro de codificação que fará com que o provedor de serviços não seja bem-funcionamento. Para corrigir esse erro, abra o arquivo MDSPEnumStorage.cpp instalado na pasta caminho de instalação do *SDK* do <  > \\ WMFSDK95 \\ \\ MDSP mdsp, vá para a linha \\ 185 e altere a seguinte linha:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Para isso:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Compile o MsHDSP.dll arquivo. Você pode fazer isso usando NMAKE ou Visual Studio. Consulte Compilando o provedor de serviços de exemplo usando [NMAKE ou](compiling-the-sample-service-provider-using-nmake.md) [compilando](compiling-the-sample-service-provider-using-visual-studio.md) o provedor de serviços de exemplo usando Visual Studio para saber como compilar o aplicativo.
2.  Registre MsHDSP.dll usando regsvr32. A seguinte linha, digitada em uma janela de prompt de comando na mesma pasta que MsHDSP.dll, registrará o provedor de serviços de exemplo:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Para parar de representar um dispositivo, insira a seguinte linha no prompt de comando:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  Os dispositivos removíveis personificados por essa DLL só podem ser vistos pelo aplicativo de exemplo fornecido com esse SDK. Compile o aplicativo de exemplo usando um dos métodos descritos em [Aplicativo de Área de Trabalho de Exemplo.](sample-desktop-application.md)
4.  Para depurar o provedor de serviços com Visual Studio, abra o provedor de serviços no Visual Studio e selecione Iniciar **no** menu **Depurar.** Na caixa de diálogo pop-up, navegue até o aplicativo de exemplo criado na etapa anterior e clique em **OK** e o provedor de serviços começará a ser executado no modo de depuração.

    Para executar o provedor de serviços sem depurar no Visual Studio, basta registrar o msdhsp.dll e executar o aplicativo de área de trabalho de exemplo que acompanha o SDK. O aplicativo da área de trabalho de exemplo executa o provedor de serviços de exemplo automaticamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> </dl>

 

 




