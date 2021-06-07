---
description: A primeira etapa no mapeamento de um arquivo é abrir o arquivo chamando a função CreateFile.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Criando um objeto de mapeamento de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502c484dd0466b47a87f4db205d1da5499bf5ef
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432498"
---
# <a name="creating-a-file-mapping-object"></a>Criando um objeto de mapeamento de arquivo

A primeira etapa no mapeamento de um arquivo é abrir o arquivo chamando a [**função CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea) Para garantir que outros processos não podem gravar na parte do arquivo mapeado, você deve abrir o arquivo com acesso exclusivo. Além disso, o identificador de arquivo deve permanecer aberto até que o processo não precise mais do objeto de mapeamento de arquivo. Uma maneira fácil de obter acesso exclusivo é especificar zero no *parâmetro fdwShareMode* de **CreateFile.** O identificador retornado **por CreateFile** é usado pela [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) para criar um objeto de mapeamento de arquivo.

A [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) retorna um identificador para o objeto de mapeamento de arquivo. Esse handle será usado ao criar [uma exibição de arquivo](creating-a-file-view.md) para que você possa acessar a memória compartilhada. Quando você chama **CreateFileMapping**, especifica um nome de objeto, o número de bytes a serem mapeados do arquivo e a permissão de leitura/gravação para a memória mapeada. O primeiro processo que chama **CreateFileMapping** cria o objeto de mapeamento de arquivo. Os processos **que chamam CreateFileMapping** para um objeto existente recebem um identificador para o objeto existente. Você pode saber se uma chamada bem-sucedida para **CreateFileMapping** criou ou abriu o objeto de mapeamento de arquivo chamando a [**função GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) **GetLastError** retorna **NO \_ ERROR** para o processo de criação e **ERROR ALREADY EXISTS \_ \_ para** processos subsequentes.

A [**função CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) falhará se os sinalizadores de acesso entrarem em conflito com aqueles especificados quando a [**função CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) abriu o arquivo. Por exemplo, para ler e gravar no arquivo:

-   **Especifique \_ os valores** **GENERIC READ e GENERIC \_ WRITE** no *parâmetro fdwAccess* de [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea).
-   **Especifique o valor PAGE \_ READWRITE** no *parâmetro fdwProtect* de [**CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)

A criação de um objeto de mapeamento de arquivo não confirma a memória física, ele só a reserva.

## <a name="file-mapping-size"></a>Tamanho do mapeamento de arquivo

O tamanho do objeto de mapeamento de arquivo é independente do tamanho do arquivo que está sendo mapeado. No entanto, se o objeto de mapeamento de arquivo for maior que o arquivo, o sistema expandirá o arquivo antes que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) retorne. Se o objeto de mapeamento de arquivo for menor que o arquivo, o sistema mapeará apenas o número especificado de bytes do arquivo.

Os *parâmetros dwMaximumSizeHigh* e *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) permitem que você especifique o número de bytes a serem mapeados do arquivo:

-   Quando você não quiser que o tamanho do arquivo seja altere (por exemplo, ao mapear arquivos somente leitura), chame [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) e especifique zero para *dwMaximumSizeHigh* e *dwMaximumSizeLow*. Isso cria um objeto de mapeamento de arquivo que tem exatamente o mesmo tamanho que o arquivo. Caso contrário, você deve calcular ou estimar o tamanho do arquivo concluído porque os objetos de mapeamento de arquivo são estáticos em tamanho; uma vez criado, seu tamanho não pode ser aumentado ou reduzido. Uma tentativa de mapear um arquivo com um comprimento de zero dessa maneira falha com um código de erro **DE ARQUIVO DE ERRO \_ \_ INVÁLIDO.** Os programas devem testar arquivos com um comprimento de zero e rejeitar esses arquivos.

-   O tamanho de um objeto de mapeamento de arquivo que é apoiado por um arquivo nomeado é limitado pelo espaço em disco. O tamanho de uma exibição de arquivo é limitado ao maior bloco contíguo disponível de memória virtual não reservada. Isso é, no máximo, 2 GB menos a memória virtual já reservada pelo processo.

O tamanho do objeto de mapeamento de arquivo selecionado controla a distância até o arquivo que você pode "ver" com o mapeamento de memória. Se você criar um objeto de mapeamento de arquivo com 500 Kb de tamanho, terá acesso somente aos primeiros 500 Kb do arquivo, independentemente do tamanho do arquivo. Como não custa nenhum recurso do sistema criar um objeto de mapeamento de arquivo maior, crie um objeto de mapeamento de arquivo que seja o tamanho do arquivo (de conjunto os parâmetros *dwMaximumSizeHigh* e *dwMaximumSizeLow* [**de CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) como zero), mesmo que você não espere exibir todo o arquivo. O custo nos recursos do sistema vem ao criar as exibições e acessá-las.

Você pode exibir uma parte do arquivo que não é iniciada no início do arquivo. Para obter mais informações, consulte [Criando uma exibição dentro de um arquivo](creating-a-view-within-a-file.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>
[Criando uma exibição de](creating-a-file-view.md)
</dt> <dt> 
[arquivo criando uma exibição dentro de um arquivo](creating-a-view-within-a-file.md)
</dt> </dl>


 
