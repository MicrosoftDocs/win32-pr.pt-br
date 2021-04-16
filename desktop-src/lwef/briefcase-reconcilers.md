---
title: Criando reconciliadores de porta-arquivos
description: Um porta-arquivos reconciliador fornece ao porta-os o meio para reconciliar versões diferentes de um documento.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- reconciliadores de porta-arquivos
- reconciliação
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b925e7055e15f6c7a49408aa28d147fb2eef5a7e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365857"
---
# <a name="creating-briefcase-reconcilers"></a>Criando reconciliadores de porta-arquivos

Um porta-arquivos reconciliador fornece ao porta-os o meio para reconciliar versões diferentes de um documento.

-   [Sobre reconciliadores de porta-arquivos](#about-briefcase-reconcilers)
    -   [Reconciliação](#reconciliation)
    -   [Criando um porta-arquivos reconciliador](#creating-a-briefcase-reconciler)
    -   [Interação do usuário em reconciliação](#user-interaction-in-reconciliation)
    -   [Reconciliando objetos inseridos](#reconciling-embedded-objects)
    -   [Residues](#residues)
-   [Referência do porta-arquivos](#briefcase-reconciler-reference)
    -   [Métodos e interfaces do portador Reconciler](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Sobre reconciliadores de porta-arquivos

Um porta-arquivos reconciliador combina diferentes versões de entrada de um documento para produzir uma nova versão de saída única do documento. Talvez seja necessário criar um porta-arquivos reconciliador para dar suporte ao seu tipo de documento. Esta visão geral descreve os reconciliadores de porta-arquivos e explica como criá-los.

Os seguintes tópicos são abordados:

-   [Reconciliação](#reconciliation)
-   [Criando um porta-arquivos reconciliador](#creating-a-briefcase-reconciler)
-   [Interação do usuário em reconciliação](#user-interaction-in-reconciliation)
-   [Reconciliando objetos inseridos](#reconciling-embedded-objects)
-   [Residues](#residues)

### <a name="reconciliation"></a>Reconciliação

Um documento é uma coleção de informações que podem ser copiadas e alteradas. Um documento tem versões diferentes se o conteúdo de pelo menos duas cópias do documento for diferente. A reconciliação produz uma única versão de um documento de duas ou mais versões iniciais. Normalmente, a versão reconciliada é uma combinação de informações das versões iniciais com as informações mais recentes ou mais úteis preservadas.

A reconciliação é iniciada pelo porta-os quando determina que duas ou mais cópias do mesmo documento são diferentes. O porta-arquivos, que atua como iniciador neste contexto, localiza e inicia o porta-dados Reconciler associado ao tipo de documento fornecido. O Reconciler compara os documentos e determina quais partes dos documentos manter. Alguns reconciliadores podem exigir a interação do usuário para concluir a reconciliação. Outros podem concluir a reconciliação sem interação com o usuário. O Reconciler pode estar contido em um aplicativo ou ser uma extensão implementada como uma DLL.

Alguns reconciliadores de porta-arquivos podem criar residues. Um residue é um documento, geralmente com o mesmo tipo de arquivo que o documento inicial, que contém informações não salvas na versão mesclada. Residues são normalmente usados para dar aos autores uma maneira rápida de determinar quais informações de seu documento original não estão na versão mesclada final. Se um Reconciler der suporte a residues, ele criará um residue para cada uma das versões originais do documento. Residues não são criados, a menos que o iniciador as solicite.

Alguns reconciliadores do porta-arquivos funcionam com o porta-arquivos para permitir que o usuário encerre a reconciliação. Esse é um recurso importante para um usuário que pode decidir que a reconciliação não deve continuar. Um reconciliador normalmente fornece um objeto de encerramento quando a reconciliação requer interação do usuário e pode ser demorada. Em alguns ambientes, um Reconciler pode permitir a reconciliação parcial, permitindo que um usuário suspenda temporariamente uma reconciliação e retome-a mais tarde. No entanto, o porta-arquivos não dá suporte à reconciliação parcial.

### <a name="creating-a-briefcase-reconciler"></a>Criando um porta-arquivos reconciliador

Você cria um porta-arquivos reconciliador implementando as interfaces de reconciliação. No mínimo, um Reconciler implementa a interface [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) e a interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) ou [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Como iniciador, o porta-arquivos determina quando a reconciliação é necessária e chama o método [**IReconcilableObject:: reconcilize**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) para iniciar a reconciliação.

Embora [**IReconcilableObject:: reconcilse**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) forneça um conjunto amplo de recursos de reconciliação, um porta-arquivos reconciliador executa apenas a reconciliação mínima na maioria dos casos. Em particular, o porta-os não requer o reconciliador para dar suporte à geração de residue ou para dar suporte ao objeto de encerramento. Além disso, o Reconciler realiza uma única reconciliação de cima para baixo e não deve retornar o \_ valor REC E \_ não concluído; ou seja, ele não deve tentar a reconciliação parcial.

O porta-arquivos fornece a interface [**IReconcileInitiator**](ireconcileinitiator.md) . O porta-arquivos Reconciler pode usar o método [**IReconcileInitiator:: SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) para definir o objeto de terminação. O porta-arquivos não usa identificadores de versão e não pode, portanto, fornecer versões anteriores de um documento se um reconciliador solicitá-los usando os métodos correspondentes no **IReconcileInitiator**.

O porta-arquivos passa para [**IReconcilableObject:: reconcilie**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) File monikers representando as versões do documento a ser reconciliado. O porta-arquivos reconcility obtém acesso às versões usando o método [IMoniker:: BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) ou [IMoniker:: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) . A última opção é geralmente mais rápida e recomendada. O Reconciler deve liberar qualquer objeto ou armazenamento ao qual ele seja associado.

Quando o porta-arquivos Reconciler usa [IMoniker:: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage), ele é associado ao armazenamento que é um armazenamento simples (um fluxo) ou um armazenamento estruturado definido por OLE. Se o Reconciler espera um armazenamento simples, ele deve usar IMoniker:: BindToStorage para solicitar a interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) . Se o Reconciler espera armazenamento estruturado, ele deve solicitar a interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . Em ambos os casos, ele deve solicitar acesso direto somente leitura (não Transacted) ao armazenamento; o acesso de leitura/gravação pode não estar disponível.

Um redirecionador mínimo de porta-arquivos normalmente se parece diretamente com o armazenamento das outras versões e lida com objetos incorporados de uma maneira muito primitiva, como mesclar duas versões do objeto, incluindo ambas as versões na versão de saída.

O iniciador localiza o porta-chave apropriado usando um subconjunto da lógica implementada pela função [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) para determinar o tipo de um determinado arquivo e, em seguida, procura no registro da classe Reconciler associada ao tipo de arquivo fornecido. O porta-arquivos, como outros componentes do Shell, determina o tipo de um arquivo exclusivamente pela extensão de nome de arquivo. A extensão de um arquivo deve ter um tipo de arquivo registrado para o porta-os para invocar um reconciliador para o arquivo. Você deve definir uma entrada de registro do seguinte formulário ao instalar o Reconciler.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

A classe deve ser de carregamento rápido, deve ser designada \_ MULTIPLEUSE e, a menos que os marshalers sejam fornecidos para a interface de reconciliação, deve ser um servidor em processo (contido em uma dll) em vez de um servidor local (implementado em um arquivo. exe).

### <a name="user-interaction-in-reconciliation"></a>Interação do usuário em reconciliação

Um porta-arquivos reconciliador deve tentar realizar a reconciliação sem interação com o usuário. Quanto mais automatizada a reconciliação, melhor será a percepção do usuário do processo.

Em alguns casos, a intervenção do usuário pode ser valiosa. Por exemplo, um sistema de documentos pode exigir que um usuário revise as alterações antes de aceitar a versão mesclada de um documento ou pode exigir comentários do usuário explicando as alterações que foram feitas. Nesses casos, o iniciador, não o portador de arquivos reconciliador, é responsável por consultar o usuário e executar as instruções do usuário.

Em outros casos, a intervenção do usuário pode ser necessária — por exemplo, quando duas versões foram editadas de maneiras incompatíveis. Nesses casos, o iniciador ou o porta-usuário Reconciler deve consultar o usuário para obter instruções sobre como resolver o conflito. Em geral, nenhum iniciador pode contar com a conclusão de uma reconciliação sem esperar alguma interação do usuário. Os reconciliadores, por outro lado, têm a opção de interagir com o usuário para resolver conflitos ou exigir que o iniciador faça isso.

### <a name="reconciling-embedded-objects"></a>Reconciliando objetos inseridos

Ao reconciliar um documento, o próprio porta-arquivos pode se tornar um iniciador se descobrir um objeto incorporado de um tipo que ele não possa reconciliar. Nesse caso, o reconciliador precisa reconciliar recursivamente cada um dos objetos incorporados e assumir todas as responsabilidades de um iniciador.

Para executar a recursão, o porta-arquivos reconciliador carrega o objeto e consulta a interface apropriada. O manipulador do objeto deve dar suporte à interface. Se qualquer método da interface retornar o valor OLE \_ e não \_ executado, o Reconciler deverá executar o objeto para executar a operação. Como o código para objetos inseridos não está sempre disponível, um Reconciler deve fornecer uma solução para essa condição. Por exemplo, o Reconciler pode incluir versões antigas e novas do objeto incorporado na versão reconciliada. O reconciliador não deve tentar reconciliar entre links.

O iniciador armazena as versões de documento que estão sendo mescladas. Em muitos casos, o iniciador tem acesso ao armazenamento de cada versão e salva o resultado da reconciliação usando armazenamento semelhante. Às vezes, no entanto, o iniciador pode ter um objeto na memória para o qual não há nenhuma versão persistente disponível. Essa situação pode ocorrer quando um documento que contém objetos inseridos abertos deve ser reconciliado antes de ser salvo. Nesses casos, o iniciador salva o resultado da reconciliação na versão encontrada na memória.

O iniciador usa a interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) para associar (carregar) a versão mesclada. O iniciador usará o método [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) se uma versão inicial já tiver sido criada e usará o método [IPersistStorage:: InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) para a versão inicial. Quando a versão mesclada é carregada, o iniciador usa [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar o endereço da interface [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) . Essa interface fornece ao iniciador acesso ao armazenamento do residues existente e oferece uma maneira de criar o armazenamento para qualquer novo residues. Em seguida, o iniciador direciona a interface para realizar a reconciliação. O iniciador, na verdade, consulta a interface [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) antes de IPersistStorage. Se o Reconciler der suporte a IPersistFile, o iniciador manipulará a réplica por meio do IPersistFile em vez dos métodos IPersistStorage. Isso permite a reconciliação de arquivos que não são armazenados como documentos compostos.

Quando a reconciliação for concluída, o iniciador poderá salvar a versão mesclada usando a interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) ou [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Durante a reconciliação, o porta-arquivos reconciliador cria residues conforme necessário e grava seus bits persistentes no armazenamento. Se a versão mesclada for um fluxo, a interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) passada para [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) conterá um fluxo chamado "Contents" com seu estado de armazenamento definido como STATEBITS \_ Flat. (Você pode definir os bits de estado usando o método [IStorage:: stat](/windows/win32/api/objidl/nf-objidl-istorage-stat) .) Após a mesclagem, o iniciador salva a versão mesclada gravando os dados de maneira apropriada. Ele deve garantir que STATEBITS \_ Flat esteja definido conforme apropriado para o armazenamento.

### <a name="residues"></a>Residues

O iniciador indica se ele quer residues definindo o parâmetro *pstgNewResidues* como um endereço válido ao chamar o método [**IReconcilableObject:: reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) . Se o Reconciler não oferecer suporte à criação de residues, ele deverá retornar imediatamente o \_ valor de rec E \_ NORESIDUES, a menos que o parâmetro *dwFlags* especifique o valor de **\_ NORESIDUESOK RECONCILEF** .

O porta-arquivos Reconciler retorna residues para o iniciador criando novos elementos de armazenamento e copiando-os para a matriz apontada por *pstgNewResidues*. Para residues de armazenamento estruturado, o Reconciler copia uma interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) e, para residues de armazenamento simples, ele copia uma interface de [IStream](/windows/win32/api/objidl/nn-objidl-istream) ou IStorage com o \_ conjunto de sinalizadores simples STATEBITS. O Reconciler usa IStorage para criar o armazenamento necessário, usando [IStorage:: CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) para criar um armazenamento simples para um residue que é um fluxo e [IStorage:: CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) para criar um armazenamento estruturado.

O iniciador prepara *pstgNewResidues* para que ele não contenha nenhum elemento na parte não reservada do namespace [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . O porta-arquivos Reconciler coloca cada residue em um elemento cujo nome corresponde à ordem de sua versão inicial. Por exemplo, o primeiro residue está contido em "1", o segundo em "2" e assim por diante. Se o próprio objeto reconciliado produzir um residue, ele será encontrado no elemento chamado "0".

O porta-arquivos reconciliador confirma cada um dos elementos recém-criados individualmente, garantindo que o iniciador tenha acesso às informações. No entanto, o Reconciler não confirma o próprio *pstgNewResidues* . O iniciador é responsável por confirmar isso ou descartar seu caso.

## <a name="briefcase-reconciler-reference"></a>Referência do porta-arquivos

Esta seção contém informações sobre as interfaces de reconciliação. Ao lidar com erros, um método pode retornar apenas os valores de erro que são explicitamente definidos como possíveis valores de retorno. Além disso, o método deve definir todas as variáveis cujos endereços são passados como parâmetros para **NULL** antes de retornar do erro.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Métodos e interfaces do portador Reconciler

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject:: reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 