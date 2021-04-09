---
title: Função FreeSoH (NapUtil. h)
description: Libera uma estrutura de dados SoH.
ms.assetid: 587acf64-31be-46c8-9d49-b5014c1a90ba
keywords:
- Função FreeSoH NAP
topic_type:
- apiref
api_name:
- FreeSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28409c18bf9f673c78d6df2a224cb936223edddb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086361"
---
# <a name="freesoh-function"></a>Função FreeSoH

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **FreeSoH** libera uma estrutura de dados **soh** .

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeSoH(
  _In_ SoH *soh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*soh* \[ no\]
</dt> <dd>

Um ponteiro para a estrutura de dados [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) a ser gratuito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **Em** parâmetros são alocados e liberados pelo chamador.
-   Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.
-   Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.

Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





