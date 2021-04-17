---
title: Estrutura de WINBIO_BDB_ANSI_381_HEADER (WinBio \_ Types. h)
description: Especifica informações sobre uma série de exemplos de impressão digital ou Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BDB_ANSI_381_HEADER
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811070"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>\_Estrutura de cabeçalho WINBIO BdB \_ ANSI \_ 381 \_

A estrutura de **\_ cabeçalho WINBIO BDB \_ ANSI \_ 381 \_** especifica informações sobre uma série de exemplos de impressão digital ou Palm.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**RecordLength**
</dt> <dd>

O tamanho, em bytes, dessa estrutura mais o tamanho de todas as estruturas de [**\_ registro WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) para as amostras de impressão digital ou Palm capturadas de um usuário final. Somente os seis bytes baixos são válidos.

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

Especifica o formato. Atualmente, isso deve ser 0x46495200.

</dd> <dt>

**VersionNumber**
</dt> <dd>

Especifica o número de versão. Atualmente, isso deve ser 0x30313000 que corresponde internamente a 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

Uma estrutura de [**\_ \_ formato registrada WINBIO**](winbio-registered-format.md) que contém o formato de dados registrado como um par de proprietário/tipo.

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

Contém a ID de unidade do dispositivo usado para capturar o exemplo.

</dd> <dt>

**ImageAcquisitionLevel**
</dt> <dd>

Especifica o nível de resolução no qual o exemplo é capturado.

</dd> <dt>

**HorizontalScanResolution**
</dt> <dd>

Especifica a resolução horizontal da verificação.

</dd> <dt>

**VerticalScanResolution**
</dt> <dd>

Especifica a resolução vertical da verificação.

</dd> <dt>

**HorizontalImageResolution**
</dt> <dd>

Especifica a resolução horizontal da imagem de impressão digital ou Palm capturada.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Especifica a resolução vertical da imagem de impressão digital ou Palm capturada.

</dd> <dt>

**ElementCount**
</dt> <dd>

Número de registros de dedos ou de Palm nesta estrutura.

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Contém a unidade de medida, 1 para polegadas e 2 para centímetros.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Especifica o número de bits em um pixel. Pode ser de 1 a 16 bits por pixel para cor.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Especifica o algoritmo usado para compactar a imagem de dedo ou Palm.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> </dl>

 

 





