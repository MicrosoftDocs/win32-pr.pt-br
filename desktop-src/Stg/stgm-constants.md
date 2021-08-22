---
title: Constantes STGM (ObjBase. h)
description: Sinalizadores que indicam as condições para criar e excluir o objeto e os modos de acesso do objeto.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18248e862c3d5981e9c34b29522b1cd75d2b61cf78a52613b3d28a1d2c98b4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661966"
---
# <a name="stgm-constants"></a>Constantes STGM

As constantes STGM são sinalizadores que indicam as condições para criar e excluir o objeto e os modos de acesso para o objeto. As constantes STGM estão incluídas nas interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e nas funções [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)e [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .

Esses elementos geralmente são combinados usando um operador **or**. Eles são interpretados em grupos, conforme listado na tabela a seguir. Não é válido usar mais de um elemento de um único grupo.

Use um sinalizador do grupo de criação ao criar um objeto, como com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).

Para obter mais informações sobre transacionamento, consulte a seção comentários.



| Agrupar                      | Sinalizador                         | Valor       |
|----------------------------|------------------------------|-------------|
| Access                     | **STGM \_ leitura**               | 0x00000000l |
|                            | **STGM \_ gravação**              | 0x00000001L |
|                            | **STGM \_ ReadWrite**          | 0x00000002L |
| Compartilhamento                    | **\_negação de compartilhamento de STGM \_ \_**  | 0x00000040L |
|                            | **\_leitura de \_ negação de compartilhamento de STGM \_**  | 0x00000030L |
|                            | **STGM \_ compartilhamento \_ negar \_ gravação** | 0x00000020L |
|                            | **STGM de \_ compartilhamento \_ exclusivo**   | 0x00000010L |
|                            | **\_prioridade STGM**           | 0x00040000L |
| Criação                   | **STGM \_ criar**             | 0x00001000L |
|                            | **STGM \_ converter**            | 0x00020000L |
|                            | **STGM \_ FAILIFTHERE**        | 0x00000000l |
| Transacionando             | **STGM \_ Direct**             | 0x00000000l |
|                            | **STGM \_ transacionado**         | 0x00010000L |
| Desempenho de transação | **STGM do \_ zero**          | 0x00100000L |
|                            | **STGM \_ NOsnapshot**         | 0x00200000L |
| Direto SWMR e simples     | **STGM \_ simples**             | 0x08000000L |
|                            | **STGM \_ direto \_ SWMR**       | 0x00400000L |
| Excluir na versão          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ leitura**
</dt> <dd> <dl> <dt>

0x00000000l
</dt> <dt>



Indica que o objeto é somente leitura, o que significa que não é possível fazer modificações. Por exemplo, se um objeto Stream for aberto com **STGM \_ Read**, o método [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) poderá ser chamado, mas o método [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) poderá não. Da mesma forma, se um objeto de armazenamento aberto com **STGM \_ Read**, os métodos [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) e [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) podem ser chamados, mas os métodos [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) e [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) podem não.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ gravação**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Permite salvar alterações no objeto, mas não permite o acesso a seus dados. As implementações fornecidas das interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) não dão suporte a esse modo somente gravação.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ ReadWrite**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Habilita o acesso e a modificação de dados de objeto. Por exemplo, se um objeto de fluxo for criado ou aberto nesse modo, será possível chamar ambos os [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStream:: Write**. Lembre-se de que essa constante não é um binário simples **ou** uma operação dos elementos **STGM \_ Write** e **STGM \_ Read** .


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**\_negação de compartilhamento de STGM \_ \_**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Especifica que aberturas subsequentes do objeto não têm acesso de leitura ou gravação negado. Se nenhum sinalizador do grupo de compartilhamento for especificado, esse sinalizador será assumido.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**\_leitura de \_ negação de compartilhamento de STGM \_**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Impede que outras pessoas abram subsequentemente o objeto no modo de **\_ leitura STGM** . Normalmente, ele é usado em um objeto de armazenamento raiz.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ compartilhamento \_ negar \_ gravação**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Impede que outras pessoas abram subsequentemente o objeto para acesso **STGM \_ Write** ou **STGM \_ ReadWrite** . No modo transacionado, o compartilhamento de **\_ \_ \_ gravação de negação de compartilhamento STGM** ou **STGM \_ \_ exclusivo** pode melhorar significativamente o desempenho porque eles não exigem instantâneos. Para obter mais informações sobre transacionamento, consulte a seção comentários.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM de \_ compartilhamento \_ exclusivo**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Impede que outras pessoas abram posteriormente o objeto em qualquer modo. Lembre-se de que esse valor não é uma operação unificada **ou** simples dos valores de **\_ negação STGM compartilhamento de \_ \_ leitura** e **\_ \_ negação \_** do compartilhamento de STGM. No modo transacionado, o compartilhamento de **\_ \_ \_ gravação de negação de compartilhamento STGM** ou **STGM \_ \_ exclusivo** pode melhorar significativamente o desempenho porque eles não exigem instantâneos. Para obter mais informações sobre transacionamento, consulte a seção comentários.


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_prioridade STGM**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Abre o objeto de armazenamento com acesso exclusivo à versão confirmada mais recentemente. Portanto, outros usuários não podem confirmar alterações no objeto enquanto você o abre no modo de prioridade. Você tem benefícios de desempenho para operações de cópia, mas impede que outras pessoas confirmassem alterações. Limite o tempo em que os objetos são abertos no modo de prioridade. Você deve especificar **STGM \_ Direct** e **STGM \_ Read** com o modo Priority e não pode especificar **STGM \_ DELETEONRELEASE**. **STGM \_ DELETEONRELEASE** é válido somente ao criar um objeto raiz, como com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Ele não é válido ao abrir um objeto raiz existente, como com [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex). Ele também não é válido ao criar ou abrir um subelemento, como com [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ criar**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Indica que um objeto de armazenamento ou fluxo existente deve ser removido antes que o novo objeto o substitua. Um novo objeto será criado quando esse sinalizador for especificado somente se o objeto existente tiver sido removido com êxito.

Esse sinalizador é usado ao tentar criar:

-   Um objeto de armazenamento em um disco, mas existe um arquivo com esse nome.
-   Um objeto dentro de um objeto de armazenamento, mas existe um objeto com o nome especificado.
-   Um objeto de matriz de byte, mas um com o nome especificado existe.

Esse sinalizador não pode ser usado com operações abertas, como [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) [**ou IStorage::OpenStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ CONVERT**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Cria o novo objeto preservando os dados existentes em um fluxo chamado "Conteúdo". No caso de um objeto de armazenamento ou uma matriz de byte, os dados antigos são formatados em um fluxo, independentemente de o arquivo ou matriz de byte existente atualmente conter um objeto de armazenamento em camadas. Esse sinalizador só pode ser usado ao criar um objeto de armazenamento raiz. Ele não pode ser usado em um objeto de armazenamento; por exemplo, em [**IStorage::CreateStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) Também não é válido usar esse sinalizador e o sinalizador **STGM \_ DELETEONRELEASE** simultaneamente.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**
</dt> <dd> <dl> <dt>

0x0000000L
</dt> <dt>



Faz com que a operação de criação falhe se houver um objeto existente com o nome especificado. Nesse caso, **STG \_ E \_ FILEALREADYEXISTS** é retornado. Esse é o modo de criação padrão; ou seja, se nenhum outro sinalizador de criação for especificado, **STGM \_ FAILIFTHERE** será implícito.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ DIRECT**
</dt> <dd> <dl> <dt>

0x0000000L
</dt> <dt>



Indica que, no modo direto, cada alteração em um elemento de armazenamento ou fluxo é escrita conforme ela ocorre. Esse será o padrão se **STGM \_ DIRECT** nem **STGM \_ TRANSACTED** for especificado.


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ TRANSACTED**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Indica que, no modo transacionado, as alterações serão armazenados em buffer e gravados somente se uma operação de commit explícita for chamada. Para ignorar as alterações, chame o método [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) na interface [**IStream,**](/windows/desktop/api/Objidl/nn-objidl-istream) [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)ou [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) A implementação de arquivo composto COM do **IStorage** não dá suporte a fluxos transacionados, o que significa que os fluxos podem ser abertos somente no modo direto e você não pode reverter alterações neles, no entanto, há suporte para armazenamentos transacionados. O arquivo composto, as implementações do sistema de arquivos autônomo e NTFS [**de IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) da mesma forma não são suportados por conjuntos de propriedades simples transacionados porque esses conjuntos de propriedades são armazenados em fluxos. No entanto, há suporte para a transação de conjuntos de propriedades não simples, que podem ser criados especificando o sinalizador **PROPSETFLAG \_ NONSIMPLE** no parâmetro *grfFlags* [**de IPropertySetStorage::Create.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOS PIG**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Indica que, no modo transacionado, um arquivo temporário de rascunho geralmente é usado para salvar modificações até que o **método Commit** seja chamado. Especificar **STGM \_ NOSCNCH** permite que a parte não utilizada do arquivo original seja usada como espaço de trabalho em vez de criar um novo arquivo para essa finalidade. Isso não afeta os dados no arquivo original e, em determinados casos, pode resultar em um desempenho aprimorado. Não é válido especificar esse sinalizador sem especificar **também STGM \_ TRANSACTED** e esse sinalizador só pode ser usado em uma raiz aberta. Para obter mais informações sobre o modo NoScrach, consulte a seção Comentários.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOSNAPSHOT**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Esse sinalizador é usado ao abrir um objeto de armazenamento **com STGM \_ TRANSACTED** e sem **STGM \_ SHARE \_ EXCLUSIVE** ou **STGM \_ SHARE DENY \_ \_ WRITE**. Nesse caso, especificar **STGM \_ NOSNAPSHOT** impede que a implementação fornecida pelo sistema criar uma cópia de instantâneo do arquivo. Em vez disso, as alterações no arquivo são escritas no final do arquivo. O espaço nãoutilado não é recuperado, a menos que a consolidação seja executada durante a confirmação e haja apenas um autor atual no arquivo. Quando o arquivo é aberto em nenhum modo de instantâneo, outra operação aberta não pode ser executada sem especificar **STGM \_ NOSNAPSHOT**. Esse sinalizador só pode ser usado em uma operação aberta raiz. Para obter mais informações sobre o modo NoSnapshot, consulte a seção Comentários.


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ SIMPLE**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Fornece uma implementação mais rápida de um arquivo composto em um caso limitado, mas frequentemente usado. Para obter mais informações, consulte a seção Comentários.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ DIRECT \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Dá suporte ao modo direto para operações de arquivo multireader e single-writer. Para obter mais informações, consulte a seção Comentários.


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Indica que o arquivo subjacente deve ser destruído automaticamente quando o objeto de armazenamento raiz for liberado. Esse recurso é mais útil para criar arquivos temporários. Esse sinalizador só pode ser usado ao criar um objeto raiz, como [**com StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Ele não é válido ao abrir um objeto raiz, como [**com StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)ou ao criar ou abrir um subelemento, como com [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Também não é válido usar esse sinalizador e o sinalizador STGM \_ CONVERT simultaneamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Você pode combinar esses sinalizadores, mas só pode escolher um sinalizador de cada grupo de sinalizadores relacionados. Normalmente, um sinalizador de cada um dos grupos de acesso e compartilhamento deve ser especificado para todas as funções e métodos que usam essas constantes. Sinalizadores de outros grupos são opcionais.

### <a name="transacted-mode"></a>Modo Transacionado

Quando o **sinalizador STGM \_ DIRECT** é especificado, apenas uma das seguintes combinações de sinalizadores pode ser especificada dos grupos de acesso e compartilhamento.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Esteja ciente de que o modo direto está implícito pela ausência **de STGM \_ TRANSACTED.** Ou seja, se **STGM \_ DIRECT** nem **STGM \_ TRANSACTED** for especificado, **STGM \_ DIRECT** será presumido.

Quando o **sinalizador \_ TRANSACTED STGM** é especificado, os objetos são criados ou abertos no modo transacionado. Nesse modo, as alterações em um objeto não persistem até que sejam confirmados. Por exemplo, as alterações em um objeto de armazenamento transacionado não são persistentes até que o [**método IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) seja chamado. As alterações em tal objeto de armazenamento serão perdidas se o objeto de armazenamento for liberado (versão final) antes que o método **Commit** seja chamado ou se o método [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) for chamado.

Quando um objeto é criado ou aberto no modo transacionado, a implementação deve manter os dados originais e as atualizações para esses dados, para que as atualizações possam ser revertidas, se necessário. Normalmente, isso é executado escrevendo alterações em uma área de rascunho até que elas sejam confirmadas ou criando uma cópia, chamada de instantâneo, dos dados confirmados mais recentemente.

Quando um objeto de armazenamento raiz é aberto no modo transacionado, o local e o comportamento dos dados de rascunho e as cópias de instantâneo podem ser controlados para otimizar o desempenho com os sinalizadores **STGM \_ NOS PIGCH** e **STGM \_ NOSNAPSHOT.** (Um objeto de armazenamento raiz é obtido de, por exemplo, a função [**StgOpenStorageEx;**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) um objeto de armazenamento obtido do método [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) é um objeto de substorage.) Normalmente, os dados e instantâneos de rascunho são armazenados em arquivos temporários, separados do armazenamento.

O efeito desses sinalizadores depende do número de leitores e/ou de autores que acessam o armazenamento raiz.

No caso de "single-writer", um objeto de armazenamento de modo transacionado é aberto para acesso de gravação e não pode haver nenhum outro acesso ao arquivo. Ou seja, o arquivo é aberto com **STGM \_ TRANSACTED**, acesso de **STGM \_ WRITE** ou **STGM \_ READWRITE** e compartilhamento de **STGM \_ SHARE \_ EXCLUSIVE.** Nesse caso, as alterações no objeto de armazenamento são escritas na área de rascunho. Quando essas alterações são comprometidas, elas são copiadas para o armazenamento original. Portanto, se nenhuma alteração for realmente feita no objeto de armazenamento, não haverá transferência de dados desnecessária.

No caso "multiple-writer", um objeto de armazenamento transacionado é aberto para acesso de gravação, mas é compartilhado de modo a permitir outros autores. Ou seja, o objeto de armazenamento é aberto com **STGM \_ TRANSACTED**, acesso de **STGM \_ WRITE** ou **STGM \_ READWRITE** e compartilhamento de **STGM \_ SHARE DENY \_ \_ READ**. Se o compartilhamento **de STGM \_ SHARE DENY \_ \_ NONE** for especificado, o caso será "multiple-writer, multiple-reader". Nesses casos, um instantâneo dos dados originais será feito durante a operação aberta. Portanto, mesmo que nenhuma alteração seja realmente feita no armazenamento e/ou não seja realmente aberta por outro autor simultaneamente, a transferência de dados ainda será necessária durante a abertura. Como resultado, o melhor desempenho em tempo aberto pode ser obtido abrindo o objeto de armazenamento nos modos **STGM \_ SHARE \_ DENY \_ WRITE** ou **STGM \_ SHARE \_ EXCLUSIVE.** Para obter mais informações sobre como as alterações são comprometidas quando há vários autores, consulte [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

No caso "single-writer, multiple-reader", um objeto de armazenamento transacionado é aberto para acesso de gravação, mas é compartilhado com leitores. Ou seja, o objeto de armazenamento é aberto pelo autor com **STGM \_ TRANSACTED**, acesso de **STGM \_ READWRITE** ou **STGM \_ WRITE** e compartilhamento de **STGM \_ SHARE DENY \_ \_ WRITE**. O armazenamento é aberto por leitores com **STGM \_ TRANSACTED**, acesso de **STGM \_ READ** e compartilhamento de **STGM \_ SHARE DENY \_ \_ NONE**. Nesse caso, o autor usa a área de rascunho para armazenar alterações não comprometidas. Como nos casos acima, o leitor incorre em uma penalidade de desempenho em tempo aberto enquanto uma cópia de instantâneo dos dados é criada.

Normalmente, a área de rascunho é um arquivo temporário, separado dos dados originais. Quando as alterações são comprometidas no arquivo original, os dados devem ser transferidos do arquivo temporário. Para evitar essa transferência de dados, o **sinalizador \_ NOSCNCH STGM** pode ser especificado. Quando esse sinalizador é especificado, partes do arquivo de objeto de armazenamento são usadas para a área de rascunho, em vez de um arquivo temporário separado. Como resultado, as alterações de confirmação podem ser executadas rapidamente, pois pouca transferência de dados é necessária. A desvantagem é que o arquivo de armazenamento pode se tornar maior do que seria, pois ele deve ser aumentado para ser grande o suficiente para os dados originais e para a área de rascunho. Para consolidar os dados e remover essa área desnecessária, reabra o armazenamento raiz no modo transacionado, mas sem definir o sinalizador **\_ noscratch STGM** . Em seguida, chame [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) com o sinalizador de **\_ consolidação de STGC** definido.

A área de instantâneo, como a área de rascunho, também é, normalmente, um arquivo temporário, e isso também pode ser afetado com um sinalizador STGM. Ao especificar o **sinalizador \_ nosnapshot STGM** , um arquivo de instantâneo temporário separado não é criado. Em vez disso, os dados originais nunca são modificados, mesmo se houver um ou mais gravadores por objeto. Quando as alterações são confirmadas, elas são adicionadas ao arquivo, mas os dados originais permanecem intactos. Esse modo aumenta a eficiência, pois reduz o tempo de execução eliminando a necessidade de criar um instantâneo durante a operação de abertura. No entanto, o uso desse modo pode resultar em um arquivo de armazenamento muito grande porque os dados no arquivo nunca podem ser substituídos. Esse não é um limite para o tamanho dos arquivos abertos no modo nosnapshot.

### <a name="direct-single-writer-multiple-reader-mode"></a>Gravador único direto, modo de Multiple-Reader

Conforme descrito, é possível ter um único gravador e vários leitores de um objeto de armazenamento, se esse objeto for aberto no modo transacionado. Também é possível atingir o único gravador, caso de multileitura no modo direto, especificando o sinalizador **\_ \_ SWMR direto STGM** .

No **modo \_ \_ SWMR direto do STGM** , é possível que um chamador Abra um objeto para acesso de leitura/gravação, enquanto outros chamadores simultaneamente têm o arquivo aberto para acesso somente leitura. Não é válido usar esse sinalizador em combinação com o sinalizador **\_ transacionado STGM** . Nesse modo, o gravador abre o objeto com os seguintes sinalizadores:

**STGM \_ Direct \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ share \_ DENYWRITE**

e cada um dos leitores abre o objeto com estes sinalizadores:

**STGM \_ \_SWMR direto** \| **STGM \_ ler** \| **STGM \_ compartilhamento \_ negar \_ nenhum**

Nesse modo, para modificar o objeto de armazenamento, o gravador deve obter acesso exclusivo ao objeto. Isso é possível quando todos os leitores o fecharam. O gravador usa a interface [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) para obter esse acesso exclusivo.

### <a name="simple-mode"></a>Modo simples

O modo simples (**STGM \_ simples**) é útil para aplicativos que executam operações de salvamento completas. Ele é eficiente, mas tem as seguintes restrições:

-   Não existe suporte para subarmazenamentos.
-   O objeto de armazenamento e os objetos de fluxo obtidos dele não podem ser empacotados.
-   Cada fluxo tem um tamanho mínimo. Se menos do que os bytes mínimos forem gravados em um fluxo quando o fluxo for liberado, o fluxo será estendido para o tamanho mínimo. Por exemplo, o tamanho mínimo para uma implementação de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) específica é de 4 KB. Um fluxo é criado e 1 KB é gravado nele. Na versão final desse **IStream**, o tamanho do fluxo será estendido automaticamente para 4 KB. Subsequentemente, abrir o fluxo e chamar o método [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) mostrará um tamanho de 4 KB.
-   Nem todos os métodos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) terão suporte da implementação. Para obter mais informações, consulte [implementação de arquivo composto por IStorage](istorage-compound-file-implementation.md)e [implementação de arquivo composto por IStream](istream-compound-file-implementation.md).

O [marshaling](/windows/desktop/Midl/marshaling-ole-data-types) é o processo de empacotamento, desempacotamento e envio de parâmetros de método de interface entre limites de thread ou processo dentro de uma RPC (chamada de procedimento remoto). Para obter mais informações, consulte [detalhes de marshaling](../com/marshaling-details.md) e [marshaling de interface](../com/interface-marshaling.md).

Quando um objeto de armazenamento é obtido por uma operação de criação no modo simples:

-   Elementos de fluxo podem ser criados, mas não abertos.
-   Quando um elemento de fluxo é criado chamando [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), não é possível criar outro fluxo até que esse objeto de fluxo seja liberado.
-   Depois que todos os fluxos forem gravados, chame [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) para liberar as alterações.

Quando um objeto de armazenamento é obtido por uma operação Open no modo simples:

-   É possível abrir apenas um elemento de fluxo por vez.
-   Não é possível alterar o tamanho de um fluxo chamando o método [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) ou buscando ou escrevendo além do final do fluxo. No entanto, como todos os fluxos têm um tamanho mínimo, é possível usar o fluxo até esse tamanho, mesmo que menos dados tenham sido gravados originalmente nele. Para determinar o tamanho de um fluxo, use o método [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .

Lembre-se de que, se um elemento de armazenamento for modificado por um objeto de armazenamento que não está no modo simples, não será possível, novamente, abrir esse elemento de armazenamento no modo simples.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>ObjBase. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISequentialStream:: ler**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

