---
description: Este tópico descreve como criar um aplicativo MUI típico.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizando recursos e compilando o aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810333"
---
# <a name="localizing-resources-and-building-the-application"></a>Localizando recursos e compilando o aplicativo

Este tópico descreve como criar um aplicativo MUI típico. Supõe-se que você esteja usando Microsoft Visual Studio para codificação e Microsoft Visual Studio ou a linha de comando do Visual Studio para compilação. Você deve usar um arquivo de solução. sln para seu aplicativo e dar suporte a um arquivo Resource. h para refletir o arquivo de recurso de idioma base.

> [!Note]  
> Se estiver usando a linha de comando do Visual Studio para a compilação, você usará o comando **VCBuild** para compilar o arquivo de solução.

 

Os arquivos de aplicativo são criados separadamente para cada idioma. Cada compilação cria arquivos. exe idênticos de idioma e. exe. mui específicos do idioma. Além disso, vários outros arquivos são copiados para as pastas de liberação apropriadas.

A compilação do aplicativo depende do tipo de recursos e do tipo de localização que você está usando. Para a localização de pré-compilação, você tem uma cópia do arquivo de idioma base localizado para cada idioma com suporte. Para a localização após a compilação, você pode copiar o arquivo. mui resultante da compilação do módulo executável e do recurso e fornecer as cópias para os localizadores.

> [!Note]  
> O procedimento a seguir pressupõe recursos Win32 PE com um projeto do Visual Studio criado para cada idioma. Os recursos de idioma base são fornecidos em um arquivo. rc e carregados usando um módulo de DLL. Você pode repetir o procedimento conforme necessário para compilar para todos os idiomas com suporte.

 

**Para compilar o aplicativo**

1.  Configure um projeto do Visual Studio para o idioma base.
2.  Se estiver interessado em usar um arquivo de configuração de recurso com as ferramentas de recurso, defina um conforme descrito em [preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md).
3.  Defina os parâmetros exigidos pelo utilitário de compilador RC nas páginas de propriedades do projeto em **Propriedades de configuração → recursos → linha de comando → opções adicionais**.
4.  Execute o compilador RC. O utilitário compila e divide os recursos não localizáveis e localizáveis em dois arquivos de objeto diferentes, usando dados de configuração de recursos. Nesta etapa, os recursos neutros à linguagem são vinculados a um arquivo LN. Para obter mais informações, consulte a descrição do utilitário em [utilitários de recursos](resource-utilities.md).
5.  Para vincular os recursos específicos do idioma a um arquivo. mui específico de idioma, defina um evento de pós-compilação para o projeto nas páginas de propriedade em **Propriedades de configuração → eventos de compilação → evento de pós-compilação → linha de comando**.
6.  Defina um evento de pós-compilação para aplicar o valor da soma de verificação do arquivo LN ao arquivo. mui para o idioma. Você pode usar o utilitário MUIRCT para esta etapa. Para obter mais informações, consulte a descrição do utilitário em [utilitários de recursos](resource-utilities.md).
7.  Use a linha de comando de evento de pós-compilação para adicionar comandos para copiar os arquivos na estrutura de pastas de liberação apropriada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a interface do usuário multilíngue](using-multilingual-user-interface.md)
</dt> <dt>

[Preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilitários de recursos](resource-utilities.md)
</dt> </dl>

 

 



