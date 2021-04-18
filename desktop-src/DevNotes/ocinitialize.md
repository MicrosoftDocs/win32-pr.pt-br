---
description: Inicializa o Gerenciador de componentes opcional.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Função OcInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748689"
---
# <a name="ocinitialize-function"></a>Função OcInitialize

Inicializa o Gerenciador de componentes opcional.

## <a name="syntax"></a>Sintaxe


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Retornos de chamada* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ retornos de chamada do cliente OCM**](ocm-client-callbacks.md) que especifica as funções de retorno de chamada a serem usadas pelo Gerenciador de OC para executar várias tarefas.

</dd> <dt>

*MasterOcInfName* \[ no\]
</dt> <dd>

O caminho do arquivo. inf do OC mestre.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Esse parâmetro pode ser um ou mais dos valores a seguir.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)
</dt> </dl> </dd> <dt>

*Erro* \[ de fora\]
</dt> <dd>

Se a função falhar, esse parâmetro indicará se uma mensagem de erro deve ser exibida.

</dd> <dt>

*Log* \[ do no\]
</dt> <dd>

Um identificador para o log.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o valor de contexto do Gerenciador do OC.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_retornos de chamada do cliente OCM \_**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
