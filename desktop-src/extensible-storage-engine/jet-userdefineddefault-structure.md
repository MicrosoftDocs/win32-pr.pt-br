---
description: 'Saiba mais sobre: estrutura JET_USERDEFINEDDEFAULT dados'
title: estrutura JET_USERDEFINEDDEFAULT de dados
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a8e5cfe4fadf0dead2e11787255089d251a98f67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479302"
---
# <a name="jet_userdefineddefault-structure"></a>estrutura JET_USERDEFINEDDEFAULT de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_userdefineddefault-structure"></a>estrutura JET_USERDEFINEDDEFAULT de dados

A **JET_USERDEFINEDDEFAULT** estrutura é especificada em conjunto com JET_bitColumnUserDefinedDefault para dar a uma nova coluna um valor padrão que é determinado usando um retorno de chamada. Essa técnica pode ser usada para implementar colunas computadas.

**Windows XP:** A **estrutura JET_USERDEFINEDDEFAULT** é introduzida no Windows XP.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Membros

**szCallback**

O nome de exportação da função que implementa o retorno de chamada no formato "função \! de módulo".

O retorno de chamada persiste como parte do esquema de coluna. O executável de host real e o nome de exportação da função devem persistir para habilitar a análise do endereço verdadeiro da função em tempo de execução.

O nome do módulo é o nome do binário do host que contém a função. O nome da função é o nome da exportação para essa função. Essas duas informações serão usadas pelo mecanismo de banco de dados em runtime para localizar o endereço verdadeiro do retorno de chamada executando uma chamada [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) no nome do módulo seguida por uma [chamada GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) no nome da função.

Por exemplo, se o retorno de chamada fosse implementado em uma DLL chamada MyCallback.DLL e essa DLL fosse armazenada em C: MyApplication e a função que implementasse o retorno de chamada fosse exportada da DLL como UserDefinedDefaultCallback, a cadeia de caracteres necessária seria \\ "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Observação**  Inserido " \! " Não há suporte para caracteres na parte do módulo do nome do retorno de chamada.

É altamente recomendável que você use um nome de retorno de chamada que não seja uma função da arquitetura do host. Por exemplo, não use exportações decoradas como stdcall ( ) porque essa convenção de chamada só tem suporte UserDefinedDefaultCallback@32 em máquinas x86. Se esse retorno de chamada tiver sido usado, o banco de dados só poderá ser usado em um computador x86. Um alias deve ser usado para fazer uma exportação de plataforma e diagnóstico nesse caso.

É altamente recomendável que você use o caminho completo do nome do módulo que está implementando o retorno de chamada. Se um caminho relativo for usado, o processo que está hospedando o banco de dados poderá ser suscetível a ataques por um binário não relacionado.

O aplicativo deve passar somente retornos de chamada confiáveis para o mecanismo de banco de dados. O mecanismo de banco de dados carregará o binário para verificar sua existência quando a coluna associada for criada. Se o caminho para o binário não for validado ou conhecido como confiável, ele poderá atacar o processo que está hospedando o banco de dados.

**pbUserData**

Um bloco independente de dados definidos pelo usuário a serem passados para o retorno de chamada quando invocado. O bloco de dados fornecido persistirá como parte do esquema de coluna. Como resultado, o bloco de dados deve ser totalmente independente e não pode se referir a nenhum dado que está fora do escopo do banco de dados.

Se **pbUserData** for zero, o valor **de cbUserData** será ignorado. Nesse caso, nenhum dado definido pelo usuário será passado para o retorno de chamada quando invocado.

**cbUserData**

Consulte **pbUserData**.

**szDependantColumns**

Reservado para uso futuro.

Esse membro sempre deve ser definido como NULL.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) <strong>e JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
