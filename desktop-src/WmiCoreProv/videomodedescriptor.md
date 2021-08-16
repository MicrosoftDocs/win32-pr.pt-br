---
description: Contém elementos de descritor de modo para a matriz MonitorSourceModes na classe WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Classe VideoModeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a8f103bf5a23f6e157fc9ecca697c0d1ce7c47bd71be20458d816ca74819dc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558401"
---
# <a name="videomodedescriptor-class"></a>Classe VideoModeDescriptor

A classe WMI **VideoModeDescriptorVideo** contém elementos de descritor de modo para a matriz **MonitorSourceModes** na [**classe WmiMonitorListedSupportedSourceModes.**](wmimonitorlistedsupportedsourcemodes.md) Esses elementos incluem recursos de monitor, como taxa de atualização, características de pixel ou tamanho da imagem. A **classe VideoModeDescriptorVideo** contém informações que são um superconjunto dos dados disponíveis de blocos de tempo estabelecidos, padrão e detalhados.

## <a name="syntax"></a>Sintaxe

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a>Membros

A **classe VideoModeDescriptor** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe VideoModeDescriptor** tem essas propriedades.

<dl> <dt>

**CompositePolarityType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de polaridade composta. Essa é a polaridade dos pulsos de sincronização horizontal fora da sincronização vertical.



| Valor                                                                              | Significado                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | A polaridade composta é positiva.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | A polaridade composta é negativa.<br/>                                 |
| <dl> <dt>2 (0x2)</dt> </dl> | Não aplicável. O tipo de sincronização de sinal deve ser composto digital.<br/> |



 

</dd> <dt>

**HorizontalActivePixels**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de pixels horizontalmente ativos.

</dd> <dt>

**HorizontalBlankingPixels**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de pixels em branco horizontalmente

</dd> <dt>

**HorizontalBorder**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Borda horizontal.

</dd> <dt>

**HorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho horizontal da imagem em milímetros (mm).

</dd> <dt>

**HorizontalPolarityType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de polaridade horizontal.



| Valor                                                                              | Significado                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | A polaridade horizontal é positiva.<br/>                               |
| <dl> <dt>1 (0x1)</dt> </dl> | A polaridade horizontal é negativa.<br/>                               |
| <dl> <dt>2 (0x2)</dt> </dl> | Não aplicável. O tipo de sincronização de sinal deve ser separado digitalmente.<br/> |



 

</dd> <dt>

**HorizontalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Denominador de taxa de atualização horizontal.

</dd> <dt>

**HorizontalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Numerador de taxa de atualização horizontal em Hertz (Hz).

</dd> <dt>

**HorizontalSyncOffset**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Deslocamento de sincronização horizontal.

</dd> <dt>

**HorizontalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Largura do pulso de sincronização horizontal.

</dd> <dt>

**IsInterlaced**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o modo de exibição está entrelaçado.

</dd> <dt>

**IsSerrationRequired**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica que tipo de serração é necessário, se apropriado.



| Valor                                                                              | Significado                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | O controlador deve fornecer sincronização horizontal durante a sincronização vertical.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | O controlador não deve fornecer sincronização horizontal durante a sincronização vertical.<br/>                             |
| <dl> <dt>2 (0x2)</dt> </dl> | Não aplicável. O tipo de sincronização de sinal deve ser composite, composição análoga ou composição digital.<br/> |



 

</dd> <dt>

**IsSyncOnRGB**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica quais linhas de sinal de vídeo devem ser sincronizadas, se apropriado.



| Valor                                                                              | Significado                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | O pulso de sincronização deve aparecer em todas as três linhas de sinal de vídeo.<br/>                  |
| <dl> <dt>1 (0x1)</dt> </dl> | O pulso de sincronização só deve aparecer na linha verde do sinal de vídeo.<br/>          |
| <dl> <dt>2 (0x2)</dt> </dl> | Não aplicável. O tipo de sincronização de sinal deve ser composto bipolar analógico.<br/> |



 

</dd> <dt>

**PixelClockRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Taxa de relógio de pixel em Hertz (Hz).

</dd> <dt>

**StereoModeType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de modo estéreo. A tabela a seguir lista os valores possíveis.



| Valor                                                                              | Significado                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Sem estéreo.<br/>                                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Estéreo sequencial de campo com imagem direita na sincronização de estéreo.<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Campo estéreo sequencial com imagem esquerda na sincronização de estéreo.<br/>  |
| <dl> <dt>3 (0x3)</dt> </dl> | Estéreo intercalado de 2 vias com imagem direita em linhas pares.<br/> |
| <dl> <dt>4 (0x4)</dt> </dl> | Estéreo intercalado de 2 vias com imagem esquerda em linhas pares.<br/>  |
| <dl> <dt>5 (0x5)</dt> </dl> | Estéreo intercalado de 4 vias.<br/>                                |
| <dl> <dt>6 (0x6)</dt> </dl> | Estéreo intercalado lado a lado.<br/>                         |



 

</dd> <dt>

**SyncSignalType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de sincronização de sinal. A tabela a seguir lista os valores possíveis.



| Valor                                                                              | Significado                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Composto analógico<br/>         |
| <dl> <dt>1 (0x1)</dt> </dl> | Bipolar analógico composto<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | Composto digital<br/>        |
| <dl> <dt>3 (0x3)</dt> </dl> | Separado digital<br/>         |



 

</dd> <dt>

**VerticalActivePixels**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de pixels ativos verticalmente.

</dd> <dt>

**VerticalBlankingPixels**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de pixels em branco verticalmente.

</dd> <dt>

**VerticalBorder**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Borda vertical.

</dd> <dt>

**VerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho vertical da imagem em milímetros (mm).

</dd> <dt>

**VerticalPolarityType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de polaridade vertical.



| Valor                                                                              | Significado                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | A polaridade vertical é positiva.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | A polaridade vertical é negativa<br/>                                  |
| <dl> <dt>2 (0x2)</dt> </dl> | Não aplicável. O tipo de sincronização de sinal deve ser separado digitalmente.<br/> |



 

</dd> <dt>

**VerticalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Denominador de taxa de atualização vertical.

</dd> <dt>

**VerticalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Numerador de taxa de atualização vertical em Hertz (Hz).

</dd> <dt>

**VerticalSyncOffset**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Deslocamento de sincronização vertical.

</dd> <dt>

**VerticalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Largura vertical de pulso de sincronização.

</dd> <dt>

VideoStandardType
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo padrão de vídeo.



| Valor                                                                                | Significado                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Outro<br/>                                                                                               |
| <dl> <dt>1 (0x1)</dt> </dl>   | VESA DMT. Na especificação de tempos do monitor de exibição da VESA (Video Electronics Standard Association).<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>   | VESA GTF. Do padrão de fórmula de tempo generalizado VESA.<br/>                                            |
| <dl> <dt>3 (0x3)</dt> </dl>   | Padrão de temporizações de vídeo coordenado VESA CVT/da VESA.<br/>                                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5)</dt> </dl>   | LARANJA<br/>                                                                                               |
| <dl> <dt>6 (0x6)</dt> </dl>   | NTSC M<br/>                                                                                              |
| <dl> <dt>7 (0x7)</dt> </dl>   | J NTSC<br/>                                                                                              |
| <dl> <dt>8 (0x8)</dt> </dl>   | NTSC 433<br/>                                                                                            |
| <dl> <dt>9 (0x9)</dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xA)</dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB)</dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xC)</dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD)</dt> </dl>  | PAL I<br/>                                                                                               |
| <dl> <dt>14 (0xE)</dt> </dl>  | PAL D<br/>                                                                                               |
| <dl> <dt>15 (0xF)</dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10)</dt> </dl> | NC DE PAL<br/>                                                                                              |
| <dl> <dt>17 (0x11)</dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12)</dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13)</dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14)</dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15)</dt> </dl> | SECAM K<br/>                                                                                             |
| <dl> <dt>22 (0x16)</dt> </dl> | SECAM K1<br/>                                                                                            |
| <dl> <dt>23 (0x17)</dt> </dl> | SECAM L<br/>                                                                                             |
| <dl> <dt>24 (0x18)</dt> </dl> | SECAM L1<br/>                                                                                            |
| <dl> <dt>25 (0x19)</dt> </dl> | EIA861<br/>                                                                                              |
| <dl> <dt>26 (0x1A)</dt> </dl> | EIA861A<br/>                                                                                             |
| <dl> <dt>27 (0x1B)</dt> </dl> | EIA861B<br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




