---
description: A função GetNPPBlobTable recupera uma tabela de BLOB NPP que representa as NICs de registro no computador local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Função GetNPPBlobTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828963"
---
# <a name="getnppblobtable-function"></a>Função GetNPPBlobTable

A função **GetNPPBlobTable** recupera uma tabela de blob NPP que representa as NICs de registro no computador local.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFilterBlob* \[ no\]
</dt> <dd>

Identificador para um BLOB de filtro que limita os BLOBs NPP retornados na tabela.

</dd> <dt>

*ppBlobTable* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura de [ \_ tabela de blob](blob-table.md) que contém pelo menos um ponteiro de BLOB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                | Descrição                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ NPP \_ dll**</dt> </dl>         | Nenhuma dll foi encontrada no diretório NPP<br/>                    |
| <dl> <dt>**NMERR \_ não \_ há \_ DLLs NPP válidas \_**</dt> </dl> | Nenhuma das DLLs no diretório NPP era uma DLL NPP válida.<br/>  |
| <dl> <dt>**NMERR \_ nenhum \_ \_ NPPS correspondente**</dt> </dl>   | BLOBs NPP foram descobertos, mas nenhum passou no teste de filtro.<br/> |
| <dl> <dt>**NMERR \_ fora \_ do \_ memorandor**</dt> </dl>       | Monitor de Rede não pôde alocar memória.<br/>            |



 

## <a name="remarks"></a>Comentários

O BLOB nomeado por *hFilterBlob* também pode ser um blob especial.

Se você definir o sinalizador no BLOB de filtro como **true**, a tabela de blob retornada também poderá incluir BLOBs especiais.

Se o BLOB nomeado por *hFilterBlob* for um blob especial, a interface do usuário do monitor de rede tentará processá-lo. Por exemplo, suponha que uma chamada anterior retorne um BLOB especial do NPP remoto. O aplicativo insere a marca necessária, nome do computador \_ . Em seguida, o Finder passa esse BLOB para o NPP remoto, que retorna uma tabela dos BLOBs NPP associados ao nome do computador.

Para destruir todos os BLOBs retornados e a tabela de BLOBs, o chamador é responsável por chamar a função **DestroyBlob** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




