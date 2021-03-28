---
description: Este tópico descreve como usar o verificador de tipo de arquivo que é fornecido no SDK do Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Como usar o verificador de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104172379"
---
# <a name="how-to-use-the-file-type-verifier"></a>Como usar o verificador de tipo de arquivo

Este tópico descreve como usar o verificador de tipo de arquivo que é fornecido no [SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Se o programa criar os tipos de arquivo com os quais os usuários devem interagir do shell do Windows (normalmente armazenados na pasta conhecida de um usuário, como **meus documentos**), é muito importante testar seu aplicativo e verificar se os arquivos que ele cria estão corretamente registrados e fornecer uma experiência de usuário de alta qualidade ao procurar e Pesquisar arquivos. Isso é especialmente importante se você espera que os usuários executem seus aplicativos no Windows 7, que se baseiam em manipuladores de tipo de arquivo de alta qualidade para muitos dos recursos do Shell.

Para verificar o tipo de arquivo usando o verificador de tipo de arquivo, siga estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Instale o aplicativo em seu ambiente de teste e copie o verificador de tipo de arquivo para esse ambiente. O verificador de tipo de arquivo está disponível no [SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

### <a name="step-2"></a>Etapa 2:

Use seu aplicativo para criar um arquivo a ser testado.

### <a name="step-3"></a>Etapa 3:

Inicie o verificador de tipo de arquivo.

### <a name="step-4"></a>Etapa 4:

Selecione a categoria para o tipo de arquivo, conforme mostrado na captura de tela a seguir.

![Captura de tela que mostra a função de arrastar e soltar.](images/file-assoc/filetypeverifier1.png)

A seleção de categoria determina o conjunto de testes que serão executados pela ferramenta. Se o seu tipo puder se enquadrar em mais de uma categoria (por exemplo, um arquivo TIF pode ser uma imagem ou um documento, dependendo do conteúdo), execute a ferramenta novamente com cada categoria apropriada.

### <a name="step-5"></a>Etapa 5:

Usando o Windows Explorer, localize um arquivo a ser testado e use o mouse para arrastá-lo para o destino no verificador de tipo de arquivo, conforme mostrado na captura de tela a seguir.

![captura de tela mostrando a função de arrastar e soltar](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Etapa 6:

Aguarde até que a ferramenta de verificação de tipo de arquivo continue em uma série de testes. O progresso do teste é mostrado pela barra de progresso, como na captura de tela a seguir.

![captura de tela mostrando a barra de progresso](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Etapa 7:

Examine o resumo dos resultados dos testes de tipo de arquivo de documento, conforme mostrado na captura de tela a seguir.

![captura de tela mostrando Resumo dos resultados](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Etapa 8:

Clique em qualquer um dos resultados na página Resumo para exibir o log detalhado. Um log de exemplo para um Gerenciador de visualização é mostrado na captura de tela a seguir.

![captura de tela mostrando log do Gerenciador de visualização](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Etapa 9:

Para salvar uma cópia do arquivo de log, clique em **salvar arquivo de log** na parte inferior da exibição do log e escolha um local apropriado para armazená-lo em seu computador.

### <a name="step-10"></a>Etapa 10:

Se as falhas forem relatadas, faça as alterações apropriadas em seu aplicativo e execute a ferramenta novamente para verificar se as falhas não estão mais aparecendo nos testes. Se os avisos forem relatados, avalie-os e decida se eles são relevantes para o tipo de arquivo específico e faça as alterações apropriadas em seu aplicativo, conforme necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



