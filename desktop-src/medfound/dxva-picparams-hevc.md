---
description: Fornece os parâmetros de nível de imagem de uma imagem compactada para decodificação de vídeo HEVC.
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: Estrutura de DXVA_PicParams_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089745"
---
# <a name="dxva_picparams_hevc-structure"></a>Estrutura de HEVC de DXVA \_ PicParams \_

Fornece os parâmetros de nível de imagem de uma imagem compactada para decodificação de vídeo HEVC.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a>Membros

<dl> <dt>

**PicWidthInMinCbsY**
</dt> <dd></dd> <dt>

**PicHeightInMinCbsY**
</dt> <dd></dd> <dt>

**croma \_ formato \_ IDC**
</dt> <dd></dd> <dt>

**\_sinalizador de \_ plano de cores separado \_** 
</dt> <dd></dd> <dt>

**profundidade de bits \_ \_ Luma \_ minus8** 
</dt> <dd></dd> <dt>

**profundidade de bits \_ \_ croma \_ minus8**
</dt> <dd></dd> <dt>

**log2 \_ Max de \_ ordem de PIC \_ \_ \_ LSB \_ minus4**
</dt> <dd></dd> <dt>

**NoPicReorderingFlag** 
</dt> <dd></dd> <dt>

 **NoBiPredFlag** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**wFormatAndSequenceInfoFlags**
</dt> <dd></dd> <dt>

**CurrPic**
</dt> <dd></dd> <dt>

**\_máximo de \_ \_ minus1 de \_ buffer da \_ PIC do SPS**
</dt> <dd></dd> <dt>

**log2 \_ min \_ Luma \_ tamanho de bloco de codificação \_ \_ \_ minus3**
</dt> <dd></dd> <dt>

**\_ \_ tamanho máximo de \_ \_ bloco de \_ codificação \_ Luma \_ dif log2 diff**
</dt> <dd></dd> <dt>

**\_tamanho do \_ bloco de transformação log2 Min \_ \_ \_ minus2**
</dt> <dd></dd> <dt>

**\_ \_ tamanho máximo de \_ \_ bloco de \_ transformação \_ de log2 dif. mínimo**
</dt> <dd></dd> <dt>

**máximo \_ de \_ profundidade de hierarquia de transformação \_ \_ entre**
</dt> <dd></dd> <dt>

**profundidade máxima de \_ hierarquia de transformação \_ \_ \_ intra**
</dt> <dd></dd> <dt>

**\_conjuntos de \_ \_ img de referência de curto prazo de \_ núm \_**
</dt> <dd></dd> <dt>

**n º de \_ \_ \_ \_ \_ controladoras de referências de referência de longo prazo**
</dt> <dd></dd> <dt>

**num \_ RefType \_ \_ L0 \_ Default \_ Active \_ minus1**
</dt> <dd></dd> <dt>

**núm \_ ref \_ IDX de \_ L1 \_ padrão \_ Active \_ minus1**
</dt> <dd></dd> <dt>

**Init \_ QP \_ minus26**
</dt> <dd></dd> <dt>

**ucNumDeltaPocsOfRefRpsIdx**
</dt> <dd></dd> <dt>

**wNumBitsForShortTermRPSInSlice**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**\_ \_ sinalizador habilitado da lista de dimensionamento \_**
</dt> <dd></dd> <dt>

**\_sinalizador habilitado para amp \_**
</dt> <dd></dd> <dt>

**\_sinalizador de deslocamento adaptável de exemplo \_ \_ habilitado \_**
</dt> <dd></dd> <dt>

**\_sinalizador habilitado para PCM \_** 
</dt> <dd></dd> <dt>

**intensidade de bit de exemplo de PCM \_ \_ \_ \_ Luma \_ minus1** 
</dt> <dd></dd> <dt>

**intensidade de bit de exemplo de PCM \_ \_ \_ \_ croma \_ minus1** 
</dt> <dd></dd> <dt>

**log2 \_ min \_ \_ Luma de \_ tamanho de bloco de codificação \_ \_ \_ minus3** 
</dt> <dd></dd> <dt>

**\_ \_ tamanho máximo do \_ \_ bloco de \_ codificação Luma do PCM \_ \_ log2 dif \_**
</dt> <dd></dd> <dt>

**\_sinalizador de filtro de loop PCM \_ \_ desabilitado \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ sinalizador atual de referências de referência de longo prazo \_** 
</dt> <dd></dd> <dt>

**\_ \_ sinalizador habilitado para MVP temporal \_ do \_ SPS**
</dt> <dd></dd> <dt>

**sinalizador de forte \_ \_ suavização \_ habilitada \_** 
</dt> <dd></dd> <dt>

**sinalizador de segmentos de fatia dependentes \_ \_ \_ habilitados \_** 
</dt> <dd></dd> <dt>

**sinalizador de sinalizador de saída \_ \_ presente \_** 
</dt> <dd></dd> <dt>

**número \_ de \_ bits extras do cabeçalho de fatia \_ \_** 
</dt> <dd></dd> <dt>

**\_sinalizador para ocultar dados de sinalização \_ \_ habilitado \_**
</dt> <dd></dd> <dt>

**\_sinalizador CABAC Init \_ Present \_**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**dwCodingParamToolFlags**
</dt> <dd></dd> <dt>

**\_ \_ sinalizador de Pred restrito \_**
</dt> <dd></dd> <dt>

**\_sinalizador de ignorar transformação \_ habilitado \_**
</dt> <dd></dd> <dt>

**\_sinalizador cu \_ QP \_ habilitado \_**
</dt> <dd></dd> <dt>

**\_ \_ \_ \_ sinalizador presente de deslocamentos do PPS Slice croma QP \_ \_**
</dt> <dd></dd> <dt>

**\_sinalizador Pred ponderado \_**
</dt> <dd></dd> <dt>

**\_sinalizador bipred ponderado \_**
</dt> <dd></dd> <dt>

**sinalizador de \_ bypass \_ habilitado de transquantity \_**
</dt> <dd></dd> <dt>

**\_sinalizador habilitado para blocos \_** 
</dt> <dd></dd> <dt>

**\_ \_ sinalizador habilitado para sincronização de codificação de \_ entropia \_** 
</dt> <dd></dd> <dt>

**\_sinalizador de espaçamento uniforme \_** 
</dt> <dd></dd> <dt>

**filtro de loop \_ \_ no \_ \_ sinalizador habilitado para blocos \_** 
</dt> <dd></dd> <dt>

**filtro de loop do PPS \_ \_ \_ no \_ \_ sinalizador habilitado para fatias \_**
</dt> <dd></dd> <dt>

**sinalizador de desbloqueio de \_ substituição de filtro \_ \_ habilitado \_**
</dt> <dd></dd> <dt>

**\_sinalizador de desbloqueio de filtro do PPS \_ \_ desabilitado \_**
</dt> <dd></dd> <dt>

**\_sinalizador de modificação \_ presente \_ de lista**
</dt> <dd></dd> <dt>

**sinalizador de extensão de cabeçalho de segmento de fatia \_ \_ \_ \_ presente \_**
</dt> <dd></dd> <dt>

**IrapPicFlag**
</dt> <dd></dd> <dt>

**IdrPicFlag** 
</dt> <dd></dd> <dt>

**IntraPicFlag** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**dwCodingSettingPicturePropertyFlags**
</dt> <dd></dd> <dt>

**deslocamento do PPS \_ CB \_ QP \_**
</dt> <dd></dd> <dt>

**deslocamento do PPS \_ CR \_ QP \_**
</dt> <dd></dd> <dt>

**\_colunas de bloco num \_ \_ minus1**
</dt> <dd></dd> <dt>

**número \_ de \_ linhas de bloco \_ minus1**
</dt> <dd></dd> <dt>

**\_minus1 de largura da coluna \_**
</dt> <dd></dd> <dt>

**altura da linha \_ \_ minus1**
</dt> <dd></dd> <dt>

**comparação \_ cu \_ QP \_ de \_ profundidade Delta**
</dt> <dd></dd> <dt>

**div2 de deslocamento do PPS \_ beta \_ \_**
</dt> <dd></dd> <dt>

**\_div2 de \_ deslocamento de TC do PPS \_**
</dt> <dd></dd> <dt>

**log2 \_ de \_ nível de mesclagem paralela \_ \_ minus2**
</dt> <dd></dd> <dt>

**CurrPicOrderCntVal**
</dt> <dd></dd> <dt>

**RefPicList**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**PicOrderCntValList**
</dt> <dd></dd> <dt>

**RefPicSetStCurrBefore**
</dt> <dd></dd> <dt>

**RefPicSetStCurrAfter**
</dt> <dd></dd> <dt>

**RefPicSetLtCurr**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**StatusReportFeedbackNumber**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




