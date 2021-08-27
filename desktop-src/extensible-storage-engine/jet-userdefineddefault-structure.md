---
description: 'Saiba mais sobre: estrutura de JET_USERDEFINEDDEFAULT'
title: Estrutura de JET_USERDEFINEDDEFAULT
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
ms.openlocfilehash: e8c34c7677a100488dfbc533aed3ca07f5b3af4c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988089"
---
# <a name="jet_userdefineddefault-structure"></a>Estrutura de JET_USERDEFINEDDEFAULT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_userdefineddefault-structure"></a>Estrutura de JET_USERDEFINEDDEFAULT

A estrutura de **JET_USERDEFINEDDEFAULT** é especificada em conjunto com JET_bitColumnUserDefinedDefault para dar uma nova coluna um valor padrão que é determinado usando um retorno de chamada. Essa técnica pode ser usada para implementar colunas computadas.

**Windows XP:** a estrutura de **JET_USERDEFINEDDEFAULT** é introduzida no Windows XP.

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

O nome de exportação da função que implementa o retorno de chamada no \! formato "função de módulo".

O retorno de chamada persiste como parte do esquema de coluna. O executável real do host e o nome de exportação da função devem persistir para habilitar a pesquisa do endereço verdadeiro da função em tempo de execução.

O nome do módulo é o nome do binário do host que contém a função. O nome da função é o nome da exportação para essa função. Essas duas informações serão usadas pelo mecanismo de banco de dados em tempo de execução para localizar o endereço verdadeiro do retorno de chamada, executando uma chamadas [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) no nome do módulo seguido por uma chamada de [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) no nome da função.

Por exemplo, se o retorno de chamada tiver sido implementado em uma DLL chamada MyCallback.DLL e essa DLL fosse armazenada em C: \\ MyApplication e a função que implementa o retorno de chamada fosse exportada da dll como UserDefinedDefaultCallback, a cadeia de caracteres necessária seria "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Observação**  Inserido " \! " Não há suporte para caracteres na parte do módulo do nome do retorno de chamada.

É altamente recomendável que você use um nome de retorno de chamada que não seja uma função da arquitetura do host. Por exemplo, não use exportações decoradas como stdcall ( UserDefinedDefaultCallback@32 ) porque essa Convenção de chamada só tem suporte em computadores x86. Se um retorno de chamada for usado, o banco de dados só poderá ser usado em um computador x86. Um alias deve ser usado para fazer uma exportação independente de plataforma nesse caso.

É altamente recomendável que você use o caminho completo do nome do módulo que está implementando o retorno de chamada. Se um caminho relativo for usado, o processo que está hospedando o banco de dados poderá ser suscetível a ataques por um binário não autorizado.

O aplicativo deve passar apenas retornos de chamada confiáveis para o mecanismo de banco de dados. O mecanismo de banco de dados carregará o binário para verificar sua existência quando a coluna associada for criada. Se o caminho para o binário não for validado ou conhecido como confiável, ele poderá atacar o processo que está hospedando o banco de dados.

**pbUserData**

Um bloco autocontido de dados definidos pelo usuário a ser passado para o retorno de chamada quando invocado. O bloco de dados fornecido continuará como parte do esquema de coluna. Como resultado, o bloco de dados deve ser totalmente independente e não pode se referir a todos os dados que estão fora do escopo do banco de dados.

Se **pbUserData** for zero, o valor de **cbUserData** será ignorado. Nesse caso, nenhum dado definido pelo usuário será passado para o retorno de chamada quando for invocado.

**cbUserData**

Consulte **pbUserData**.

**szDependantColumns**

Reservado para uso futuro.

Esse membro sempre deve ser definido como nulo.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) e <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
