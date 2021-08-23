---
title: Criando reconciliadores de pastas
description: Um reconciliador de pastas fornece à Pasta os meios para reconciliar versões diferentes de um documento.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- reconciliadores de pastas
- Reconciliação
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4161796999172e6ee9bc7c403e723f9f8bafe7e876b544888fa5e7105b724f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556936"
---
# <a name="creating-briefcase-reconcilers"></a>Criando reconciliadores de pastas

Um reconciliador de pastas fornece à Pasta os meios para reconciliar versões diferentes de um documento.

-   [Sobre reconciliadores de pastas](#about-briefcase-reconcilers)
    -   [Reconciliação](#reconciliation)
    -   [Criando um reconciliador de pastas](#creating-a-briefcase-reconciler)
    -   [Interação do usuário na reconciliação](#user-interaction-in-reconciliation)
    -   [Reconciliando objetos inseridos](#reconciling-embedded-objects)
    -   [Resíduos](#residues)
-   [Referência de reconciliador de pastas](#briefcase-reconciler-reference)
    -   [Interfaces e métodos reconciliadores de pasta](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Sobre reconciliadores de pastas

Um reconciliador de pastas combina diferentes versões de entrada de um documento para produzir uma única versão de saída do documento. Talvez seja necessário criar um reconciliador de pastas para dar suporte ao tipo de documento. Esta visão geral descreve os reconciliadores de pastas e explica como crie-os.

Os seguintes tópicos são abordados:

-   [Reconciliação](#reconciliation)
-   [Criando um reconciliador de pastas](#creating-a-briefcase-reconciler)
-   [Interação do usuário na reconciliação](#user-interaction-in-reconciliation)
-   [Reconciliando objetos inseridos](#reconciling-embedded-objects)
-   [Resíduos](#residues)

### <a name="reconciliation"></a>Reconciliação

Um documento é uma coleção de informações que podem ser copiadas e alteradas. Um documento terá versões diferentes se o conteúdo de pelo menos duas cópias do documento for diferente. A reconciliação produz uma única versão de um documento de duas ou mais versões iniciais. Normalmente, a versão reconciliada é uma combinação de informações das versões iniciais com as informações mais recentes ou mais úteis preservadas.

A reconciliação é iniciada pela Pasta quando determina que duas ou mais cópias do mesmo documento são diferentes. A pasta, que atua como o iniciador nesse contexto, localiza e inicia o reconciliador de pasta associado ao tipo de documento determinado. O reconciliador compara os documentos e determina quais partes dos documentos reter. Alguns reconciliadores podem exigir interação do usuário para concluir a reconciliação. Outros podem concluir a reconciliação sem interação do usuário. O reconciliador pode estar contido em um aplicativo ou ser uma extensão implementada como uma DLL.

Alguns reconciliadores de pastas podem criar reações. Um documento é um documento, geralmente com o mesmo tipo de arquivo que o documento inicial, que contém informações não salvas na versão mesclada. Normalmente, os resíduos são usados para dar aos autores uma maneira rápida de determinar quais informações do documento original não estão na versão mesclada final. Se um reconciliador dá suporte a resíduos, ele cria um problema para cada uma das versões originais do documento. Os resíduos não são criados, a menos que o iniciador as solicita.

Alguns reconciliadores de pastas trabalham com a Pasta para permitir que o usuário enceencer a reconciliação. Esse é um recurso importante para um usuário que pode decidir que a reconciliação não deve continuar. Um reconciliador normalmente fornece um objeto de encerramento quando a reconciliação requer interação do usuário e pode ser longa. Em alguns ambientes, um reconciliador pode permitir a reconciliação parcial, permitindo que um usuário suspenda temporariamente uma reconciliação e retome-a mais tarde. No entanto, atualmente, a pasta não dá suporte à reconciliação parcial.

### <a name="creating-a-briefcase-reconciler"></a>Criando um reconciliador de pastas

Você cria um reconciliador de pastas implementando as interfaces de reconciliação. No mínimo, um reconciliador implementa a interface [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) e a interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) [ou IPersistFile.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Como iniciador, a Pasta determina quando a reconciliação é necessária e chama o método [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) para iniciar a reconciliação.

Embora [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) fornece um amplo conjunto de recursos de reconciliação, um reconciliador de pastas realiza apenas a reconciliação mínima na maioria dos casos. Em particular, a Pasta não exige que o reconciliador dá suporte à geração de resíduos ou para dar suporte ao objeto de encerramento. Além disso, o reconciliador realiza uma única reconciliação de cima para baixo e não deve retornar o valor REC \_ E NOTCOMPLETE; ou seja, ele não deve tentar a reconciliação \_ parcial.

A pasta fornece a interface [**IReconcileInitiator.**](ireconcileinitiator.md) O reconciliador de pastas pode usar o método [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) para definir o objeto de encerramento. A pasta não usa identificadores de versão e, portanto, não pode fornecer versões anteriores de um documento se um reconciliador as solicitar usando os métodos correspondentes **em IReconcileInitiator**.

A pasta passa para os monikers de arquivo [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) que representam as versões do documento a serem reconciliadas. O reconciliador de pastas obtém acesso às versões usando o método [IMoniker::BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) ou [IMoniker::BindToStorage.](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) O último é geralmente mais rápido e é recomendado. O reconciliador deve liberar qualquer objeto ou armazenamento ao qual se vincula.

Quando o reconciliador de pastas usa [IMoniker::BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage), ele se vincula ao armazenamento que é um armazenamento simples (um fluxo) ou um armazenamento estruturado definido pelo OLE. Se o reconciliador espera armazenamento simples, ele deve usar IMoniker::BindToStorage para solicitar a interface [IStream.](/windows/win32/api/objidl/nn-objidl-istream) Se o reconciliador espera armazenamento estruturado, ele deve solicitar a interface [IStorage.](/windows/win32/api/objidl/nn-objidl-istorage) Em ambos os casos, ele deve solicitar acesso direto somente leitura (não traduzido) ao armazenamento; O acesso de leitura/gravação pode não estar disponível.

Um reconciliador mínimo de pastas normalmente analisa diretamente o armazenamento de outras versões e lida com objetos inseridos de maneira muito primitiva, como mesclar duas versões do objeto incluindo ambas as versões na versão de saída.

O iniciador localiza o reconciliador de pasta apropriado usando um subconjunto da lógica implementada pela função [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) para determinar o tipo de um determinado arquivo e, em seguida, procura no Registro a classe reconciliadora associada ao tipo de arquivo determinado. A pasta, como outros componentes do Shell, determina o tipo de um arquivo exclusivamente pela extensão de nome de arquivo. A extensão de um arquivo deve ter um tipo de arquivo registrado para a Pasta para invocar um reconciliador para o arquivo. Você deve definir uma entrada do Registro do formulário a seguir ao instalar o reconciliador.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

A classe deve ser de carregamento rápido, deve ser designada multipleUSE e, a menos que marshalers sejam fornecidos para a interface de reconciliação, deve ser um servidor em processo (contido em uma DLL) em vez de um servidor local (implementado em um \_ arquivo .exe).

### <a name="user-interaction-in-reconciliation"></a>Interação do usuário na reconciliação

Um reconciliador de pastas deve tentar realizar a reconciliação sem interação do usuário. Quanto mais automatizada a reconciliação, melhor a percepção do usuário sobre o processo.

Em alguns casos, a intervenção do usuário pode ser valiosa. Por exemplo, um sistema de documentos pode exigir que um usuário revise as alterações antes de aceitar a versão mesclada de um documento ou pode exigir comentários do usuário explicando as alterações feitas. Nesses casos, o iniciador, não o reconciliador de pastas, é responsável por consultar o usuário e realizar as instruções do usuário.

Em outros casos, a intervenção do usuário pode ser necessária, por exemplo, quando duas versões foram editadas de maneiras incompatíveis. Nesses casos, o iniciador ou o reconciliador deve consultar o usuário para obter instruções sobre como resolver o conflito. Em geral, nenhum iniciador pode contar com a conclusão de uma reconciliação sem esperar alguma interação do usuário. Reconciliadores, por outro lado, têm a opção de interagir com o usuário para resolver conflitos ou exigir que o iniciador faça isso.

### <a name="reconciling-embedded-objects"></a>Reconciliando objetos inseridos

Ao reconciliar um documento, o reconciliador em si pode se tornar um iniciador se descobrir um objeto inserido de um tipo que ele não pode reconciliar. Nesse caso, o reconciliador precisa reconciliar recursivamente cada um dos objetos inseridos e assumir todas as responsabilidades de um iniciador.

Para realizar a recursão, o reconciliador de pasta carrega o objeto e as consultas para a interface apropriada. O manipulador do objeto deve dar suporte à interface . Se qualquer método da interface retornar o valor OLE \_ E NOTRUNNING, o reconciliador deverá executar o objeto para \_ executar a operação. Como o código para objetos inseridos nem sempre está disponível, um reconciliador deve fornecer uma solução para essa condição. Por exemplo, o reconciliador pode incluir versões antigas e novas do objeto inserido na versão reconciliada. O reconciliador não deve tentar reconciliar entre links.

O iniciador armazena as versões do documento que estão sendo mescladas. Em muitos casos, o iniciador tem acesso ao armazenamento de cada versão e salva o resultado da reconciliação usando armazenamento semelhante. Às vezes, no entanto, o iniciador pode ter um objeto na memória para o qual nenhuma versão persistente está disponível. Essa situação pode ocorrer quando um documento que contém objetos inseridos abertos deve ser reconciliado antes de ser salvo. Nesses casos, o iniciador salva o resultado da reconciliação na versão encontrada na memória.

O iniciador usa a interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) para vincular (carregar) a versão mesclada. O iniciador usará o método [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) se uma versão inicial já tiver sido criada e usar o método [IPersistStorage::InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) para a versão inicial. Quando a versão mesclada é carregada, o iniciador usa [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar o endereço da interface [**IReconcilableObject.**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) Essa interface fornece ao iniciador acesso ao armazenamento dos resíduos existentes e fornece uma maneira de criar armazenamento para quaisquer novos resíduos. Em seguida, o iniciador direciona a interface para realizar a reconciliação. Na verdade, o iniciador consulta a interface [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) antes de IPersistStorage. Se o reconciliador for compatível com IPersistFile, o iniciador manipulará a réplica por meio do IPersistFile em vez dos métodos IPersistStorage. Isso permite a reconciliação de arquivos que não são armazenados como documentos compostos.

Quando a reconciliação for concluída, o iniciador poderá salvar a versão mesclada usando a interface [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) ou [IPersistFile.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Durante a reconciliação, o reconciliador cria reações conforme necessário e grava seus bits persistentes no armazenamento. Se a versão mesclada for um fluxo, a interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) passada para [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) conterá um fluxo chamado "Conteúdo" com seu estado de armazenamento definido como STATEBITS \_ FLAT. (Você pode definir os bits de estado usando o [método IStorage::Stat.)](/windows/win32/api/objidl/nf-objidl-istorage-stat) Após a mesclagem, o iniciador salva a versão mesclada escrevendo os dados de maneira apropriada. Ele deve garantir que STATEBITS \_ FLAT seja definido conforme apropriado para o armazenamento.

### <a name="residues"></a>Resíduos

O iniciador indica se deseja retalhes definindo o parâmetro *pstgNewResidues* como um endereço válido ao chamar o [**método IReconcilableObject::Reconcile.**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) Se o reconciliador não dá suporte à criação de resíduos, ele deve retornar imediatamente o valor REC E NORESIDUES, a menos que o parâmetro \_ \_ *dwFlags* especifique o **valor RECONCILEF \_ NORESIDUESOK.**

O reconciliador de pastas retorna reações ao iniciador criando novos elementos de armazenamento e copiando-os para a matriz apontada por *pstgNewResidues*. Para estruturas de armazenamento estruturado, o reconciliador copia uma interface [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) e, para estruturas de armazenamento simples, copia uma interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) ou IStorage com o sinalizador STATEBITS \_ FLAT definido. O reconciliador usa o IStorage para criar o armazenamento necessário, usando [IStorage::CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) para criar um armazenamento simples para um vazamento que é um fluxo e [IStorage::CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) para criar armazenamento estruturado.

O iniciador prepara *pstgNewResidues* para que ele não contenha elementos na parte não reservada do namespace [IStorage.](/windows/win32/api/objidl/nn-objidl-istorage) O reconciliador de pastas coloca cada resíduos em um elemento cujo nome corresponde à ordem de sua versão inicial. Por exemplo, o primeiro está contido em "1", o segundo em "2" e assim por diante. Se o próprio objeto reconciliado produzir um resíduos, ele será encontrado no elemento chamado "0".

O reconciliador de pastas confirma cada um dos elementos recém-criados individualmente, garantindo que o iniciador tenha acesso às informações. No entanto, o reconciliador não confirma *pstgNewResidues em* si. O iniciador é responsável por fazer isso ou, de outra forma, descartar isso.

## <a name="briefcase-reconciler-reference"></a>Referência de reconciliador de pastas

Esta seção contém informações sobre as interfaces de reconciliação. Ao tratar erros, um método pode retornar somente os valores de erro definidos explicitamente como valores de retorno possíveis. Além disso, o método deve definir todas as variáveis cujos endereços são passados como parâmetros para **NULL** antes de retornar do erro.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Interfaces e métodos reconciliadores de pasta

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 