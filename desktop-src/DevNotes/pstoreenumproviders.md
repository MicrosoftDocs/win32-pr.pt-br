---
description: Obtém um objeto enumerador que pode ser usado, por sua vez, para enumerar os provedores de armazenamento protegidos que estão atualmente instalados no sistema.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Função PStoreEnumProviders (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748494"
---
# <a name="pstoreenumproviders-function"></a>Função PStoreEnumProviders

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtém um objeto enumerador que pode ser usado, por sua vez, para enumerar os provedores de armazenamento protegidos que estão atualmente instalados no sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*ppenum* 
</dt> <dd>

Um ponteiro para um ponteiro para uma interface [**IEnumPStoreProviders**](ienumpstoreproviders.md) que pode ser usada para enumerar provedores instalados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna um **HRESULT**.

## <a name="remarks"></a>Comentários

O componente de armazenamento protegido tem uma arquitetura baseada em provedor. Os aplicativos que fazem uso do armazenamento protegido podem especificar quais dos provedores instalados usar ao armazenar e recuperar seus dados.

A função **PStoreEnumProviders** é usada para enumerar os provedores de armazenamento protegidos instalados. Cada provedor é identificado por um GUID (identificador global exclusivo).

Até este momento, apenas um provedor de armazenamento protegido já foi escrito. Considerando que o serviço de armazenamento protegido está preterido no momento, é muito improvável que todos os provedores adicionais sejam produzidos. Como resultado, essa função não deve ser usada para nenhuma finalidade.

Esta função não tem biblioteca de importação associada; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
