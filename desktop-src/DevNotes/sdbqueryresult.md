---
description: Contém os resultados da consulta do banco de dados Shim para um executável correspondente.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Estrutura SDBQUERYRESULT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920263"
---
# <a name="sdbqueryresult-structure"></a>Estrutura SDBQUERYRESULT

Contém os resultados da consulta do banco de dados Shim para um executável correspondente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**atrExes**
</dt> <dd>

Os valores de **TAGREF** dos arquivos executáveis correspondentes. Observe que **sdb \_ Max \_ EXES** é definido como 16.

</dd> <dt>

**adwExeFlags**
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

**atrLayers**
</dt> <dd>

Os valores de **TAGREF** das camadas correspondentes. Observe que **as \_ \_ camadas sdb Max** são definidas como 8.

</dd> <dt>

**dwLayerFlags**
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

**trApphelp**
</dt> <dd>

O valor **TAGREF** da mensagem AppHelp do executável correspondente.

</dd> <dt>

**dwExeCount**
</dt> <dd>

O número de elementos em **atrExes**.

</dd> <dt>

**dwLayerCount**
</dt> <dd>

O número de elementos em **atrLayers**.

</dd> <dt>

**guidID**
</dt> <dd>

O GUID do último arquivo executável.

</dd> <dt>

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

**dwCustomSDBMap**
</dt> <dd>

Um mapa dos bancos de dados de shims personalizados. Os bits correspondentes serão definidos se **rgGuidDB** for válido.

</dd> <dt>

**rgGuidDB**
</dt> <dd>

Os GUIDs dos bancos de dados de Shim. Observe que **sdb \_ Max \_ SDBS** é definido como 16.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




