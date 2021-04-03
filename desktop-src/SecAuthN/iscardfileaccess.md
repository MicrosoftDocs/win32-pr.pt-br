---
description: A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um provedor de serviço de cartão inteligente.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interface ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828959"
---
# <a name="iscardfileaccess-interface"></a>Interface ISCardFileAccess

\[A interface **ISCardFileAccess** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviço*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) .

A interface **ISCardFileAccess** pode ser usada para implementar uma interface de alto nível para um sistema de arquivos baseado em cartão com um sistema de arquivos de cartão subjacente com base na estrutura definida no ISO/IEC 7816-4. Outras implementações são possíveis, mas isso deve ser o mais comum.

A interface **ISCardFileAccess** pode ser usada para expor entidades do sistema de arquivos de uma maneira muito familiar para os desenvolvedores de aplicativos no ambiente do PC. Ele fornece mecanismos para localizar arquivos específicos e executar operações comuns, como seleção, leitura, gravação, criação e exclusão. Ele encapsula e mascara muitos dos detalhes de baixo nível envolvidos na execução dessas operações no nível do cartão.

Veja a seguir um uso típico da interface **ISCardFileAccess** . Nesse caso, a interface **ISCardFileAccess** é usada para selecionar, abrir e gravar em um arquivo.

**Para gravar em um arquivo**

1.  Chame [**ISCardManage:: createfileaccess**](iscardmanage-createfileaccess.md) para criar uma interface **ISCardFileAccess** .
2.  Chame [**Open**](iscardfileaccess-open.md) para selecionar e abrir o arquivo.
3.  Chamar [**gravação**](iscardfileaccess-write.md).
4.  Chame [**fechar**](iscardfileaccess-close.md).
5.  Libere a interface **ISCardFileAccess** .

## <a name="members"></a>Membros

A interface **ISCardFileAccess** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardFileAccess** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardFileAccess** tem esses métodos.



| Método                                                              | Descrição                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeDir**](iscardfileaccess-changedir.md)                     | Altera o diretório do cartão inteligente atual para o novo diretório especificado.<br/>                                                          |
| [**Inclui**](iscardfileaccess-close.md)                             | Fecha o arquivo especificado.<br/>                                                                                                        |
| [**Criada**](iscardfileaccess-create.md)                           | Cria um arquivo em um determinado local dentro do sistema de arquivos ICC.<br/>                                                                    |
| [**Apagar**](iscardfileaccess-delete.md)                           | Exclui um arquivo especificado.<br/>                                                                                                         |
| [**Diretório**](iscardfileaccess-directory.md)                     | Recupera uma lista de arquivos.<br/>                                                                                                        |
| [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)             | Retorna um caminho absoluto para o diretório selecionado no momento.<br/>                                                                     |
| [**GetFileCapabilities**](iscardfileaccess-getfilecapabilities.md) | Recupera recursos de arquivo.<br/>                                                                                                      |
| [**GetProperties**](iscardfileaccess-getproperties.md)             | Recupera os dados primitivos referenciados por marcas para o objeto especificado.<br/>                                                           |
| [**Invalidar**](iscardfileaccess-invalidate.md)                   | Torna o arquivo especificado inválido.<br/>                                                                                               |
| [**Abrir**](iscardfileaccess-open.md)                               | Abre o arquivo especificado para uso posterior.<br/>                                                                                         |
| [**Ler**](iscardfileaccess-read.md)                               | Lê e retorna os dados especificados de um determinado arquivo.<br/>                                                                           |
| [**Rehabilitate**](iscardfileaccess-rehabilitate.md)               | Cria um arquivo (EF ou DF), que anteriormente não é válido usando o comando Invalidate, acessível pelo aplicativo.<br/> |
| [**Seek**](iscardfileaccess-seek.md)                               | Seleciona o objeto do qual a permissão de leitura/gravação será feita.<br/>                                                                 |
| [**SetProperties**](iscardfileaccess-setproperties.md)             | Define os dados primitivos referenciados por marcas para o objeto especificado.<br/>                                                                |
| [**Gravar**](iscardfileaccess-write.md)                             | Grava dados em um arquivo aberto atual.<br/>                                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



 

 
