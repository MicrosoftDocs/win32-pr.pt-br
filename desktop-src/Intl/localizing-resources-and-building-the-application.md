---
description: Este tópico descreve como criar um aplicativo de MUI típico.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizando recursos e criando o aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490fde8e0b6d9381b346409efad1501331be71d2d4e958be050274dc0428fe62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788496"
---
# <a name="localizing-resources-and-building-the-application"></a>Localizando recursos e criando o aplicativo

Este tópico descreve como criar um aplicativo de MUI típico. Supõe-se que você está usando Microsoft Visual Studio para codificação e Microsoft Visual Studio ou a Visual Studio de comando para criação. Supõe-se que você use um arquivo de solução .sln para seu aplicativo e dê suporte a um arquivo Resource.h para refletir o arquivo de recurso de linguagem base.

> [!Note]  
> Se estiver usando a Visual Studio de comando para o build, você usará o **comando vcbuild** para criar o arquivo de solução.

 

Os arquivos de aplicativo são construídos separadamente para cada idioma. Cada build cria arquivos .exe e específicos do idioma .exe.mui idênticos. Além disso, vários outros arquivos são copiados para as pastas de versão apropriadas.

O build do aplicativo depende do tipo de recursos e do tipo de localização que você está usando. Para a localização de pré-build, você tem uma cópia do arquivo de linguagem base localizado para cada idioma com suporte. Para a localização pós-build, você pode copiar o arquivo .mui resultante do build do módulo executável e de recurso e fornecer as cópias para os localizadores.

> [!Note]  
> O procedimento a seguir pressu que os recursos do Win32 PE com um Visual Studio projeto criado para cada idioma. Os recursos de linguagem base são fornecidos em um arquivo .rc e carregados usando um módulo DLL. Você pode repetir o procedimento conforme necessário para criar todos os idiomas com suporte.

 

**Para criar o aplicativo**

1.  Configurar um projeto Visual Studio para a linguagem base.
2.  Se estiver interessado em usar um arquivo de configuração de recurso com as ferramentas de recurso, desenvolva um conforme descrito em Preparando um [arquivo de configuração de recurso.](preparing-a-resource-configuration-file.md)
3.  Definir parâmetros exigidos pelo utilitário compilador RC nas páginas de propriedades do projeto em Propriedades de Configuração → Recursos → linha de comando **→ opções adicionais**.
4.  Execute o Compilador RC. O utilitário compila e divide os recursos não localizáveis e localizáveis em dois arquivos de objeto diferentes, usando dados de configuração de recurso. Nesta etapa, os recursos neutros em idioma são vinculados a um arquivo LN. Para obter mais informações, consulte a descrição do utilitário em [Utilitários de Recursos](resource-utilities.md).
5.  Para vincular os recursos específicos do idioma a um arquivo .mui específico a um idioma, de definir um evento de pós-build para o projeto nas páginas de propriedades em Propriedades de Configuração → Eventos de Build → Evento **pós-build → Linha** de Comando .
6.  De configurar um evento de pós-build para aplicar o valor da verificação do arquivo LN ao arquivo .mui para o idioma. Você pode usar o utilitário LTDCT para esta etapa. Para obter mais informações, consulte a descrição do utilitário em [Utilitários de Recursos](resource-utilities.md).
7.  Use a linha de comando de evento pós-build para adicionar comandos para copiar os arquivos na estrutura de pasta de versão apropriada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Interface de Usuário Multilíngue](using-multilingual-user-interface.md)
</dt> <dt>

[Preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilitários de recursos](resource-utilities.md)
</dt> </dl>

 

 



