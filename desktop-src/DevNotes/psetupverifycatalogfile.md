---
description: Verifica um único arquivo de catálogo usando a política de assinatura de código do sistema operacional padrão, como a assinatura de driver.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: Função pSetupVerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 5c7ad6e866fd82773ab55e57011e14c1cfae2dd47d6f5c91a772eab9cfce42c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386226"
---
# <a name="psetupverifycatalogfile-function"></a>Função pSetupVerifyCatalogFile

\[Essa função não é mais suportada pela Microsoft. Para um arquivo INF (instalação do dispositivo), os desenvolvedores devem usar **SetupVerifyInfFile**. Para validar um catálogo não baseado em INF, use **WinVerifyTrust**.\]

Verifica um único arquivo de catálogo usando a política de assinatura de código do sistema operacional padrão, como a assinatura de driver.

## <a name="syntax"></a>Sintaxe


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CatalogFullPath* \[ Em\]
</dt> <dd>

O caminho totalmente qualificado do arquivo de catálogo a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará **ERROR \_ SUCCESS**; caso contrário, retornará o erro de [**WinVerifyTrust.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetupVerifyInfFile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
