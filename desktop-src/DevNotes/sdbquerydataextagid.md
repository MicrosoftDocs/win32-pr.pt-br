---
description: Recupera dados das entradas especificadas que pertencem a uma entrada EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Função SdbQueryDataExTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 19477385fb70f65c560d1a13d479fc4c2ce1853220aff6ac32a75f3634a40d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815376"
---
# <a name="sdbquerydataextagid-function"></a>Função SdbQueryDataExTagID

Recupera dados das entradas especificadas que pertencem a uma entrada EXE.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um alça para o banco de dados shim.

</dd> <dt>

*tiExe* \[ Em\]
</dt> <dd>

O [**TAGID**](tagid.md) da entrada EXE.

</dd> <dt>

*lpszDataName* \[ in, opcional\]
</dt> <dd>

O nome da entrada de dados a ser recuperada. Para especificar várias entradas, separe os nomes com o caractere de faixa invertida (" \\ "). Se esse parâmetro for **NULL,** a função tentará retornar todas as entradas de dados.

</dd> <dt>

*lpdwDataType* \[ out, opcional\]
</dt> <dd>

O tipo de dados das entradas retornadas. Esse parâmetro pode ser um dos seguintes valores:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG \_ BINARY**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ MULTI \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ NONE**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

O buffer que recebe os dados. Se o buffer não for grande o suficiente para conter os dados, a função falhará e **retornará ERROR \_ INSUFFICIENT \_ BUFFER**.

</dd> <dt>

*lpcbBufferSize* \[ in, out, opcional\]
</dt> <dd>

O tamanho do *buffer lpBuffer,* em bytes.

</dd> <dt>

*ptiData* \[ out\]
</dt> <dd>

O [**TAGID**](tagid.md) da entrada de dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna um dos valores a seguir.



| Código de retorno                                                                                                    | Descrição                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl>       | Um ou mais parâmetros de entrada estão incorretos.<br/>                  |
| <dl> <dt>**ERRO \_ INTERNO DE BANCO DE DADOS \_ \_ CORRUPÇÕES**</dt> </dl> | Nenhuma entrada de dados foi encontrada para a entrada EXE.<br/>               |
| <dl> <dt>**ERRO \_ BUFFER \_ INSUFICIENTE**</dt> </dl>     | O buffer não é grande o suficiente para conter as entradas de dados.<br/> |
| <dl> <dt>**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**</dt> </dl>      | Falha na alocação de memória.<br/>                               |
| <dl> <dt>**ERRO \_ NÃO \_ ENCONTRADO**</dt> </dl>               | Uma entrada de dados com o nome *lpszDataName* não foi encontrada.<br/>    |
| <dl> <dt>**ÊXITO \_ DO ERRO**</dt> </dl>                  | A função foi concluída com êxito.<br/>                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




