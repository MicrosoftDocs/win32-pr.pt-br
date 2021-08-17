---
title: WINBIO_BDB_ANSI_381_HEADER estrutura (Tipos \_ winbio.h)
description: Especifica informações sobre uma série de amostras de impressão digital ou de mão.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER estrutura Windows API do Biometric Framework
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
ms.openlocfilehash: 3bc9eee5d3ca99799c76b849e7b990eee2b94c61309c4d729f736ad33a00eecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911274"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>Estrutura DE \_ HEADER WINBIO BDB \_ ANSI \_ 381 \_

A **estrutura DE HEADER DO WINBIO \_ BDB \_ ANSI \_ 381 \_** especifica informações sobre uma série de amostras de impressão digital ou de coquelinha.

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

**Recordlength**
</dt> <dd>

O tamanho, em bytes, dessa estrutura mais o tamanho de todas as estruturas [**WINBIO \_ BDB \_ ANSI \_ 381 \_ RECORD**](winbio-bdb-ansi-381-record.md) para a impressão digital ou amostras de mão capturadas de um usuário final. Somente os seis bytes baixos são válidos.

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

Uma [**estrutura WINBIO \_ REGISTERED \_ FORMAT**](winbio-registered-format.md) que contém o formato de dados registrado como um par proprietário/tipo.

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

Especifica a resolução horizontal da impressão digital capturada ou da imagem de mão.

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

Especifica a resolução vertical da impressão digital capturada ou da imagem de mão.

</dd> <dt>

**ElementCount**
</dt> <dd>

Número de registros de dedo ou de mão nessa estrutura.

</dd> <dt>

**ScaleUnits**
</dt> <dd>

Contém a unidade de medida, 1 para polegadas e 2 para centímetros.

</dd> <dt>

**PixelDepth**
</dt> <dd>

Especifica o número de bits em um pixel. Isso pode ser de 1 a 16 bits por pixel para cor.

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

Especifica o algoritmo usado para compactar a imagem do dedo ou da mão.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> </dl>

 

 





