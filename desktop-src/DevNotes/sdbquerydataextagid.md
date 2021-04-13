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
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370360"
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

*PDB* \[ no\]
</dt> <dd>

Um identificador para o banco de dados de Shim.

</dd> <dt>

*tiExe* \[ no\]
</dt> <dd>

O [**TagId**](tagid.md) da entrada exe.

</dd> <dt>

*lpszDataName* \[ em, opcional\]
</dt> <dd>

O nome da entrada de dados a ser recuperada. Para especificar várias entradas, separe os nomes com o caractere de barra invertida (" \\ "). Se esse parâmetro for **nulo**, a função tentará retornar todas as entradas de dados.

</dd> <dt>

*lpdwDataType* \[ out, opcional\]
</dt> <dd>

O tipo de dados das entradas retornadas. Esse parâmetro pode ser um dos seguintes valores:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**\_binário reg**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ multi \_ sz**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ None**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ sz**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ fora\]
</dt> <dd>

O buffer que recebe os dados. Se o buffer não for grande o suficiente para conter os dados, a função falhará e retornará o **\_ \_ buffer insuficiente de erro**.

</dd> <dt>

*lpcbBufferSize* \[ entrada, saída, opcional\]
</dt> <dd>

O tamanho do buffer *lpBuffer* , em bytes.

</dd> <dt>

*ptiData* \[ fora\]
</dt> <dd>

O [**TagId**](tagid.md) da entrada de dados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna um dos valores a seguir.



| Código de retorno                                                                                                    | Descrição                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>       | Um ou mais parâmetros de entrada estão incorretos.<br/>                  |
| <dl> <dt>**ERRO \_ de \_ corrupção interna do BD \_**</dt> </dl> | Não foram encontradas entradas de dados para a entrada EXE.<br/>               |
| <dl> <dt>**ERRO \_ de \_ buffer insuficiente**</dt> </dl>     | O buffer não é grande o suficiente para conter as entradas de dados.<br/> |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl>      | Falha na alocação de memória.<br/>                               |
| <dl> <dt>**ERRO \_ não \_ encontrado**</dt> </dl>               | Uma entrada de dados com o nome *lpszDataName* não foi encontrada.<br/>    |
| <dl> <dt>**êxito do erro \_**</dt> </dl>                  | A função foi concluída com êxito.<br/>                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




