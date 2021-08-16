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
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827171"
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

*Hwndparent* 
</dt> <dd>

Um alça para a janela pai.

</dd> <dt>

*Dwfoptions* 
</dt> <dd>

Uma combinação dos sinalizadores a seguir que controlam a instalação e a configuração.



| Valor                                                                                                                                                                                                                                  | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | Instale Exchange e o Internet Mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | Instale o RAS (se necessário).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | Instale o TCP/IP (se necessário).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

Se esse valor for não **NULL,** no retorno, ele será **TRUE** somente se Windows ser reiniciado para concluir a instalação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Se nenhum erro ocorrer, ele retornará o **código ERROR \_ SUCCESS.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
