---
description: Contém informações de dados AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Estrutura de APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747630"
---
# <a name="apphelp_data-structure"></a>\_Estrutura de dados APPHELP

Contém informações de dados AppHelp.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwFlags**
</dt> <dd>

Esse parâmetro pode ser um ou mais dos valores a seguir.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DESABILITAR \_ Shim** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DESABILITAR \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ \_NOUI APPHELP** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Cancelamento de APPHELP** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DESABILITAR \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DESABILITAR \_ camada** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DESABILITAR \_ Driver** (0x00000040)
</dt> </dl> </dd> <dt>

**dwSeverity**
</dt> <dd>

Esse parâmetro pode ser APPTYPE \_ nenhum (0).

</dd> <dt>

**dwHTMLHelpID**
</dt> <dd>

O identificador da ajuda HTML.

</dd> <dt>

**szAppName**
</dt> <dd>

O nome do aplicativo.

</dd> <dt>

**trExe**
</dt> <dd>

O [**TAGREF**](tagref.md) do arquivo executável correspondente.

</dd> <dt>

**szURL**
</dt> <dd>

A URL para o link online AppHelp.

</dd> <dt>

**szLink**
</dt> <dd>

O texto do link para **szURL**.

</dd> <dt>

**szAppTitle**
</dt> <dd>

O título da mensagem AppHelp.

</dd> <dt>

**szContact**
</dt> <dd>

As informações de contato do fornecedor.

</dd> <dt>

**szDetails**
</dt> <dd>

A mensagem AppHelp detalhada.

</dd> <dt>

**dwData**
</dt> <dd>

Dados definidos pelo usuário gerenciados pelo aplicativo.

</dd> <dt>

**bSPEntry**
</dt> <dd>

Esse membro será **verdadeiro** se essa entrada estiver no banco de dados Service Pack e **false** caso contrário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




