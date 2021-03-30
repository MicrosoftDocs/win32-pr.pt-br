---
title: IDirectWriterLock-implementação de arquivo composto
description: A implementação do arquivo composto do IDirectWriterLock fornece uma maneira de abrir um arquivo composto no modo direto com um único gravador e vários leitores.
ms.assetid: 4b247dae-d937-430a-bdb7-c47fa3c026b6
keywords:
- IDirectWriterLock Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861935a4c373ce03408c0e633e581e56d39623da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635219"
---
# <a name="idirectwriterlock---compound-file-implementation"></a>IDirectWriterLock-implementação de arquivo composto

A implementação do arquivo composto do [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) fornece uma maneira de abrir um arquivo composto no modo direto com um único gravador e vários leitores.

Os arquivos compostos podem ser abertos no modo direto usando o \_ sinalizador direto STGM. A interface [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) define o \_ sinalizador de \| negação de gravação STGM ReadWrite STGM \_ share \_ \_ como válido no modo direto, sem a necessidade da sobrecarga de uma cópia de instantâneo.

Quando um arquivo composto é aberto no modo transacionado usando o \_ sinalizador transacionado STGM, você também pode ter vários leitores e um único gravador usando o \_ sinalizador de gravação de \| \_ negação de compartilhamento STGM ReadWrite STGM \_ \_ . No entanto, nesse caso, uma cópia de instantâneo do arquivo é feita para os leitores. Geralmente, há uma sobrecarga de uma cópia transitória.

## <a name="when-to-use"></a>Quando usar

Use a implementação fornecida pelo sistema do [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) ao abrir um armazenamento no modo direto (STGM \_ Direct) com os sinalizadores de \_ \| gravação de \_ negação do compartilhamento STGM do STGM ReadWrite \_ \_ .

Para obter um ponteiro para [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock), chame **QueryInterface** em [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para obter o objeto de armazenamento raiz para o arquivo composto.

Chame [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) para obter acesso de gravação exclusivo a um arquivo composto. Chame [**IDirectWriterLock:: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) para liberar acesso de gravação exclusivo.

[**IDirectWriterLock:: HaveWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-havewriteaccess) indica se o arquivo está bloqueado no momento.

## <a name="remarks"></a>Comentários

A implementação do arquivo composto do recurso de gravador único e de vários leitores baseia-se no bloqueio de intervalo. O gravador obtém acesso exclusivo ao armazenamento para gravação depois que todos os leitores atuais tiverem fechado o armazenamento. Enquanto o gravador está ativo, os leitores subsequentes não podem abrir o armazenamento. O gravador chama [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) para obter acesso de gravação exclusivo. O gravador deve então chamar [**IDirectWriterLock:: ReleaseWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-releasewriteaccess) para liberar o armazenamento.

A chamada para [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess) é necessária antes de gravar neste modo de leitor único e de vários gravadores. Tentativas de gravar no arquivo sem chamar **IDirectWriterLock:: WaitForWriteAccess** primeiro resultam em STG \_ E \_ ACCESSDENIED. Esse erro é retornado mesmo se o gravador abrir o arquivo inicialmente e nenhum leitor tiver o arquivo aberto no momento.

## <a name="marshaling-considerations"></a>Considerações sobre marshaling

O empacotamento personalizado normalmente é usado quando um arquivo composto é empacotado para outro processo no mesmo computador. Ao realizar marshaling de armazenamentos, os direitos de acesso não são considerados e o ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) é passado para o novo processo com os mesmos modos de acesso e direitos que o processo de marshaling original. Para obter mais informações sobre modos de acesso, consulte [**constantes STGM**](stgm-constants.md). Durante o marshaling, nenhum bloqueio é obtido ou verificado para garantir acesso de gravação exclusivo. Nesse caso, não há nenhuma imposição da política de gravador único para arquivos compostos abertos no modo de gravador único e de vários leitores. Em vez disso, a imposição é manipulada internamente pela implementação do arquivo composto.

Como o ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) é passado para outro processo durante o marshaling, é possível que dois processos tenham acesso simultâneo ao mesmo arquivo composto. Embora um chamador possa ter obtido acesso de gravação exclusivo para o armazenamento chamando [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), a versão com marshaling também pode ter acesso simultaneamente. As versões com marshaling não são forçadas a fechar enquanto o único gravador acessa o arquivo. Nesse caso, a implementação do arquivo composto sincroniza as gravações internamente.

Se um único gravador obtiver acesso exclusivo chamando, [**IDirectWriterLock:: WaitForWriteAccess**](/windows/desktop/api/Objidl/nf-objidl-idirectwriterlock-waitforwriteaccess), o armazenamento com marshaling também terá acesso de gravação e não precisará chamar **IDirectWriterLock:: WaitForWriteAccess**. Ambos os processos têm acesso de gravação e a sincronização é controlada pela implementação do arquivo composto interno.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock)
</dt> </dl>

 

 




