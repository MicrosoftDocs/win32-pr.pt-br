---
description: Obtém o nível de uma regra de identificação de hash que corresponde ao hash especificado.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Função SaferiSearchMatchingHashRules
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457106"
---
# <a name="saferisearchmatchinghashrules-function"></a>Função SaferiSearchMatchingHashRules

Obtém o nível de uma regra de identificação de hash que corresponde ao hash especificado.

Esta função não tem biblioteca de importação associada e não está declarada em um cabeçalho público. Você deve definir um ponteiro de função com a assinatura dessa função, e deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Advapi32.dll.

É recomendável usar a função [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) para avaliar as diretivas de restrição de software.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HashAlgorithm* \[ em, opcional\]
</dt> <dd>

O identificador do algoritmo usado para criar o hash.

</dd> <dt>

*pHashBytes* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém o hash.

</dd> <dt>

*dwHashSize* \[ no\]
</dt> <dd>

O tamanho, em bytes, da matriz *pHashBytes* .

</dd> <dt>

*dwOriginalImageSize* \[ em, opcional\]
</dt> <dd>

O tamanho, em bytes, da imagem original da qual o hash foi computado.

</dd> <dt>

*pdwFoundLevel* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador de nível para a regra de identificação de hash correspondente.

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

Reservado. Defina esse valor como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True** se a função for bem-sucedida; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
