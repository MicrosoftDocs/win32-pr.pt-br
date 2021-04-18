---
description: Instala os componentes do sistema especificados.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Função IcfgInstallInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749713"
---
# <a name="icfginstallinetcomponents-function"></a>Função IcfgInstallInetComponents

Instala os componentes do sistema especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* 
</dt> <dd>

Um identificador para a janela pai.

</dd> <dt>

*dwfOptions* 
</dt> <dd>

Uma combinação dos sinalizadores a seguir que controlam a instalação e a configuração.



| Valor                                                                                                                                                                                                                                  | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | Instale o Exchange e o Internet mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | Instale o RAS (se necessário).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | Instale o TCP/IP (se necessário).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Se esse valor for não **nulo**, em retorno será **verdadeiro** somente se o Windows precisar ser reiniciado para concluir a instalação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Se nenhum erro ocorrer, ele retornará o código de **\_ êxito do erro** .

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
