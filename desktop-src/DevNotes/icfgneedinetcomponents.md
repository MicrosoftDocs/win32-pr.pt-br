---
description: Determina se os componentes marcados nas opções são instalados no sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Função IcfgNeedInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 9b0d533e234986f54c6a4de668273bda08d9c810dc9f5a93acb3aaf030cea665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390656"
---
# <a name="icfgneedinetcomponents-function"></a>Função IcfgNeedInetComponents

Determina se os componentes marcados nas opções são instalados no sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwfOptions* 
</dt> <dd>

Uma combinação dos sinalizadores a seguir que especificam quais componentes detectar da lista a seguir.



| Valor                                                                                                                                                                                                                                  | Significado                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | o Exchange ou o Internet mail é necessário?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | O RAS é necessário?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | O TCP/IP é necessário?<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

Se esse valor for não **nulo**, ele será **verdadeiro** no retorno se um ou mais componentes não estiverem instalados no sistema.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Se nenhum erro ocorrer, ele retornará o código de **\_ êxito do erro** .

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
