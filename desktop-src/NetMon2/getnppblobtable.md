---
description: A função GetNPPBlobTable recupera uma tabela NPP BLOB que representa as NICs de registro no computador local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Função GetNPPBlobTable (Netmon.h)
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
ms.openlocfilehash: 49920df1be929eb9b35781aeabdcdf47167e82a94066e2d3237207dd00b08f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910696"
---
# <a name="getnppblobtable-function"></a>Função GetNPPBlobTable

A **função GetNPPBlobTable** recupera uma tabela NPP BLOB que representa as NICs de registro no computador local.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFilterBlob* \[ Em\]
</dt> <dd>

Lidar com um BLOB de filtro que limita os BLOBs NPP retornados na tabela.

</dd> <dt>

*ppBlobTable* \[ out\]
</dt> <dd>

Ponteiro para uma [estrutura TABLE \_ DE BLOB](blob-table.md) que contém pelo menos um ponteiro BLOB.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                | Descrição                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ NPP \_ DLL**</dt> </dl>         | Nenhuma DLL foi encontrada no diretório NPP.<br/>                    |
| <dl> <dt>**NMERR \_ SEM \_ \_ \_ DLLS NPP VÁLIDAS**</dt> </dl> | Nenhuma das DLLs no diretório NPP era DLLs NPP válidas.<br/>  |
| <dl> <dt>**NMERR \_ SEM \_ \_ NPPS CORRESPONDENTE**</dt> </dl>   | BloBs NPP foram descobertos, mas nenhum passou no teste de filtro.<br/> |
| <dl> <dt>**NMERR \_ \_ FORA DO \_ MEMOR**</dt> </dl>       | Monitor de Rede foi capaz de alocar memória.<br/>            |



 

## <a name="remarks"></a>Comentários

O BLOB chamado por *hFilterBlob* também pode ser um BLOB especial.

Se você definir o sinalizador no BLOB de filtro como **TRUE,** a tabela BLOB retornada também poderá incluir BLOBs especiais.

Se o BLOB nomeado por *hFilterBlob* for um BLOB especial, o Monitor de Rede interface do usuário tentará processá-lo. Por exemplo, suponha que uma chamada anterior retorne um BLOB especial do NPP remoto. O aplicativo insere a marca necessária, MACHINE \_ NAME. Em seguida, o finder passa esse BLOB para o NPP remoto, que retorna uma tabela dos BLOBs NPP associados ao nome do computador.

Para destruir todos os BLOBs retornados e a tabela BLOB, o chamador é responsável por chamar a **função DestroyBlob.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




