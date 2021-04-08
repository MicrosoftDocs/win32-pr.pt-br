---
description: As funções global e local têm suporte para portabilidade de código de 16 bits ou para manter a compatibilidade do código-fonte com o Windows de 16 bits.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Funções globais e locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf356647f92f0e7d82e914a91020c438363ff082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827042"
---
# <a name="global-and-local-functions"></a>Funções globais e locais

As funções global e local têm suporte para portabilidade de código de 16 bits ou para manter a compatibilidade do código-fonte com o Windows de 16 bits. Começando com o Windows de 32 bits, as funções global e local são implementadas como funções de wrapper que chamam as [funções de heap](heap-functions.md) correspondentes usando um identificador para o heap padrão do processo. Portanto, as funções global e local têm maior sobrecarga do que outras funções de gerenciamento de memória.

As [funções de heap](heap-functions.md) fornecem mais recursos e controle do que as funções globais e locais. Os novos aplicativos devem usar as funções de heap, a menos que a documentação declare especificamente que uma função global ou local deve ser usada. Por exemplo, algumas funções do Windows alocam memória que deve ser liberada com [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree), e as funções globais ainda são usadas com troca dinâmica de dados (DDE), as funções da área de transferência e os objetos de dados OLE. Para obter uma lista completa das funções globais e locais, consulte a tabela em [funções de gerenciamento de memória](memory-management-functions.md).

O gerenciamento de memória do Windows não fornece um heap local separado e um heap global, como o Windows de 16 bits. Como resultado, as famílias de funções global e local são equivalentes e escolher entre elas é uma questão de preferência pessoal. Observe que a alteração de um modelo de memória segmentada de 16 bits para um modelo de memória virtual de 32 bits fez algumas das funções globais e locais relacionadas e suas opções desnecessárias ou sem sentido. Por exemplo, não há mais ponteiros próximos e distantes, porque as alocações locais e globais retornam endereços virtuais de 32 bits.

Os objetos de memória alocados por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) estão em páginas privadas e confirmadas com acesso de leitura/gravação que não podem ser acessados por outros processos. A memória alocada usando **GlobalAlloc** com **GMEM \_ Ddeshare** não é realmente compartilhada globalmente como no Windows de 16 bits. Esse valor não tem nenhum efeito e está disponível apenas para compatibilidade. Aplicativos que exigem memória compartilhada para outros fins devem usar objetos de mapeamento de arquivos. Vários processos podem mapear uma exibição do mesmo objeto de mapeamento de arquivo para fornecer a memória compartilhada nomeada. Para obter mais informações, consulte [mapeamento de arquivo](file-mapping.md).

As alocações de memória são limitadas apenas pela memória física disponível, incluindo o armazenamento no arquivo de paginação no disco. Quando você aloca memória fixa, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) retornam um ponteiro que o processo de chamada pode usar imediatamente para acessar a memória. Quando você aloca a memória móvel, o valor de retorno é um identificador. Para obter um ponteiro para um objeto de memória móvel, use as funções [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) e [**LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) .

O tamanho real da memória alocada pode ser maior que o tamanho solicitado. Para determinar o número real de bytes alocados, use a função [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) ou [**Localize**](/windows/desktop/api/WinBase/nf-winbase-localsize) . Se a quantidade alocada for maior que a quantidade solicitada, o processo poderá usar toda a quantidade.

As funções [**GlobalRealloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) e [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) alteram o tamanho ou os atributos de um objeto de memória alocado por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc). O tamanho pode aumentar ou diminuir.

As funções [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) e [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) liberam a memória alocada por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), [**GlobalRealloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)ou [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc). Para descartar o objeto de memória especificado sem invalidar o identificador, use a função [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) ou [**LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) . O identificador pode ser usado posteriormente por **GlobalRealloc** ou **LocalReAlloc** para alocar um novo bloco de memória associado ao mesmo identificador.

Para retornar informações sobre um objeto de memória especificado, use a função [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) ou [**LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) . As informações incluem a contagem de bloqueio do objeto e indica se o objeto é Descartado ou já foi Descartado. Para retornar um identificador para o objeto de memória associado a um ponteiro especificado, use a função [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) ou [**LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
