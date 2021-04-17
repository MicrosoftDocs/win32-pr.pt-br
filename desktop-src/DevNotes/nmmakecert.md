---
description: Cria um certificado de usuário para uso com a conferência do NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: Função NmMakeCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748691"
---
# <a name="nmmakecert-function"></a>Função NmMakeCert

Cria um certificado de usuário para uso com a conferência do NetMeeting.

## <a name="syntax"></a>Sintaxe


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szFirstName* 
</dt> <dd>

O nome do usuário.

</dd> <dt>

*szLastName* 
</dt> <dd>

O sobrenome do usuário.

</dd> <dt>

*szEmailName* 
</dt> <dd>

O nome de email do usuário.

</dd> <dt>

*szCity* 
</dt> <dd>

a cidade do usuário.

</dd> <dt>

*szCountry* 
</dt> <dd>

O país/região do usuário.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Um valor que indica como o certificado deve ser criado. Os valores podem ser qualquer um dos seguintes.



| Valor                                                                                                                                                                                                                                                            | Significado                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**NMMKCERT \_ \_ \_ Somente limpeza de F somente**</dt> <dt>0x00000004</dt> </dl>    | Exclua o certificado antigo sem criar um novo. <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**NMMKCERT \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt> </dl>  | Exclua o certificado antigo criado anteriormente com essa função. <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**NMMKCERT \_ F \_ \_ computador local**</dt> <dt>0x00000002</dt> </dl> | Crie o certificado no repositório de certificados do computador local. <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará 1 se a função for bem-sucedida e – 1 se a função falhar.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 
