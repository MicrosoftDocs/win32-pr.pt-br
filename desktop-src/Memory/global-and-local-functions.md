---
description: As funções globais e locais têm suporte para portação de código de 16 bits ou para manter a compatibilidade do código-fonte com Windows.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Funções globais e locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d7832f90a420e6be87fe6599cc8c9e4722ddf45b789663ed9b39eab4e5449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869686"
---
# <a name="global-and-local-functions"></a>Funções globais e locais

As funções globais e locais têm suporte para portação de código de 16 bits ou para manter a compatibilidade do código-fonte com Windows. A partir do Windows de 32 bits, as funções globais e locais são implementadas como funções wrapper que chamam as funções [de heap correspondentes](heap-functions.md) usando um alça para o heap padrão do processo. Portanto, as funções globais e locais têm maior sobrecarga do que outras funções de gerenciamento de memória.

As [funções de heap](heap-functions.md) fornecem mais recursos e controle do que as funções globais e locais. Novos aplicativos devem usar as funções de heap, a menos que a documentação adquir especificamente que uma função global ou local deve ser usada. Por exemplo, algumas funções Windows alocam memória que deve ser liberada com [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)e as funções globais ainda são usadas com Dados Dinâmicos Exchange (DDE), funções de área de transferência e objetos de dados OLE. Para ver uma lista completa de funções globais e locais, consulte a tabela em [Funções de Gerenciamento de Memória](memory-management-functions.md).

Windows gerenciamento de memória não fornece um heap local e um heap global separados, como Windows de 16 bits. Como resultado, as famílias globais e locais de funções são equivalentes e escolher entre elas é uma questão de preferência pessoal. Observe que a alteração de um modelo de memória segmentada de 16 bits para um modelo de memória virtual de 32 bits tornou algumas das funções globais e locais relacionadas e suas opções desnecessárias ou sem sentido. Por exemplo, não há mais ponteiros próximos e distantes, porque as alocações locais e globais retornam endereços virtuais de 32 bits.

Os objetos de memória alocados por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) estão em páginas privadas e confirmadas com acesso de leitura/gravação que não podem ser acessados por outros processos. A memória alocada usando **GlobalAlloc** com **GMEM \_ D LTDARE** não é realmente compartilhada globalmente, pois está em 16 bits Windows. Esse valor não tem efeito e está disponível apenas para compatibilidade. Os aplicativos que exigem memória compartilhada para outras finalidades devem usar objetos de mapeamento de arquivo. Vários processos podem mapear uma exibição do mesmo objeto de mapeamento de arquivo para fornecer memória compartilhada nomeada. Para obter mais informações, consulte [Mapeamento de arquivos](file-mapping.md).

As alocações de memória são limitadas apenas pela memória física disponível, incluindo o armazenamento no arquivo de paging no disco. Quando você aloca memória fixa, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) retornam um ponteiro que o processo de chamada pode usar imediatamente para acessar a memória. Quando você aloca memória movêvel, o valor de retorno é um handle. Para obter um ponteiro para um objeto de memória móvel, use as [**funções GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) e [**LocalLock.**](/windows/desktop/api/WinBase/nf-winbase-locallock)

O tamanho real da memória alocada pode ser maior que o tamanho solicitado. Para determinar o número real de bytes alocados, use a [**função GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) [**ou LocalSize.**](/windows/desktop/api/WinBase/nf-winbase-localsize) Se o valor alocado for maior que o valor solicitado, o processo poderá usar todo o valor.

As [**funções GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) e [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) alteram o tamanho ou os atributos de um objeto de memória alocado por [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc.**](/windows/desktop/api/WinBase/nf-winbase-localalloc) O tamanho pode aumentar ou diminuir.

As [**funções GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) e [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) liberam a memória alocada por [**GlobalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**LocalAlloc,**](/windows/desktop/api/WinBase/nf-winbase-localalloc) [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)ou [**LocalReAlloc.**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) Para descartar o objeto de memória especificado sem invalidar o identificador, use a [**função GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) ou [**LocalDiscard.**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) O handle pode ser usado posteriormente por **GlobalReAlloc** ou **LocalReAlloc** para alocar um novo bloco de memória associado ao mesmo handle.

Para retornar informações sobre um objeto de memória especificado, use a [**função GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) ou [**LocalFlags.**](/windows/desktop/api/WinBase/nf-winbase-localflags) As informações incluem a contagem de bloqueios do objeto e indicam se o objeto é descartável ou se já foi descartado. Para retornar um identificador para o objeto de memória associado a um ponteiro especificado, use a [**função GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) [**ou LocalHandle.**](/windows/desktop/api/WinBase/nf-winbase-localhandle)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comparando métodos de alocação de memória](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
