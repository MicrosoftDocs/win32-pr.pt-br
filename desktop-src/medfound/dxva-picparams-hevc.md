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
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="9e975-103">Estrutura de HEVC de DXVA \_ PicParams \_</span><span class="sxs-lookup"><span data-stu-id="9e975-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="9e975-104">Fornece os parâmetros de nível de imagem de uma imagem compactada para decodificação de vídeo HEVC.</span><span class="sxs-lookup"><span data-stu-id="9e975-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e975-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e975-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="9e975-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9e975-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e975-107">**PicWidthInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="9e975-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-108">**PicHeightInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="9e975-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-109">**croma \_ formato \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="9e975-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-110">**\_sinalizador de \_ plano de cores separado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-111">**profundidade de bits \_ \_ Luma \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="9e975-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-112">**profundidade de bits \_ \_ croma \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="9e975-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-113">**log2 \_ Max de \_ ordem de PIC \_ \_ \_ LSB \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="9e975-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-114">**NoPicReorderingFlag**</span><span class="sxs-lookup"><span data-stu-id="9e975-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="9e975-115">**NoBiPredFlag**</span><span class="sxs-lookup"><span data-stu-id="9e975-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="9e975-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-117">**wFormatAndSequenceInfoFlags**</span><span class="sxs-lookup"><span data-stu-id="9e975-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-118">**CurrPic**</span><span class="sxs-lookup"><span data-stu-id="9e975-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-119">**\_máximo de \_ \_ minus1 de \_ buffer da \_ PIC do SPS**</span><span class="sxs-lookup"><span data-stu-id="9e975-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-120">**log2 \_ min \_ Luma \_ tamanho de bloco de codificação \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="9e975-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-121">**\_ \_ tamanho máximo de \_ \_ bloco de \_ codificação \_ Luma \_ dif log2 diff**</span><span class="sxs-lookup"><span data-stu-id="9e975-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-122">**\_tamanho do \_ bloco de transformação log2 Min \_ \_ \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="9e975-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-123">**\_ \_ tamanho máximo de \_ \_ bloco de \_ transformação \_ de log2 dif. mínimo**</span><span class="sxs-lookup"><span data-stu-id="9e975-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-124">**máximo \_ de \_ profundidade de hierarquia de transformação \_ \_ entre**</span><span class="sxs-lookup"><span data-stu-id="9e975-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-125">**profundidade máxima de \_ hierarquia de transformação \_ \_ \_ intra**</span><span class="sxs-lookup"><span data-stu-id="9e975-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-126">**\_conjuntos de \_ \_ img de referência de curto prazo de \_ núm \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-127">**n º de \_ \_ \_ \_ \_ controladoras de referências de referência de longo prazo**</span><span class="sxs-lookup"><span data-stu-id="9e975-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-128">**num \_ RefType \_ \_ L0 \_ Default \_ Active \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-129">**núm \_ ref \_ IDX de \_ L1 \_ padrão \_ Active \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-130">**Init \_ QP \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="9e975-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-131">**ucNumDeltaPocsOfRefRpsIdx**</span><span class="sxs-lookup"><span data-stu-id="9e975-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-132">**wNumBitsForShortTermRPSInSlice**</span><span class="sxs-lookup"><span data-stu-id="9e975-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="9e975-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-134">**\_ \_ sinalizador habilitado da lista de dimensionamento \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-135">**\_sinalizador habilitado para amp \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-136">**\_sinalizador de deslocamento adaptável de exemplo \_ \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-137">**\_sinalizador habilitado para PCM \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-138">**intensidade de bit de exemplo de PCM \_ \_ \_ \_ Luma \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-139">**intensidade de bit de exemplo de PCM \_ \_ \_ \_ croma \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-140">**log2 \_ min \_ \_ Luma de \_ tamanho de bloco de codificação \_ \_ \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="9e975-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-141">**\_ \_ tamanho máximo do \_ \_ bloco de \_ codificação Luma do PCM \_ \_ log2 dif \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-142">**\_sinalizador de filtro de loop PCM \_ \_ desabilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-143">**\_ \_ \_ \_ sinalizador atual de referências de referência de longo prazo \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-144">**\_ \_ sinalizador habilitado para MVP temporal \_ do \_ SPS**</span><span class="sxs-lookup"><span data-stu-id="9e975-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-145">**sinalizador de forte \_ \_ suavização \_ habilitada \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-146">**sinalizador de segmentos de fatia dependentes \_ \_ \_ habilitados \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-147">**sinalizador de sinalizador de saída \_ \_ presente \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-148">**número \_ de \_ bits extras do cabeçalho de fatia \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-149">**\_sinalizador para ocultar dados de sinalização \_ \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-150">**\_sinalizador CABAC Init \_ Present \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="9e975-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-152">**dwCodingParamToolFlags**</span><span class="sxs-lookup"><span data-stu-id="9e975-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-153">**\_ \_ sinalizador de Pred restrito \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-154">**\_sinalizador de ignorar transformação \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-155">**\_sinalizador cu \_ QP \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-156">**\_ \_ \_ \_ sinalizador presente de deslocamentos do PPS Slice croma QP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-157">**\_sinalizador Pred ponderado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-158">**\_sinalizador bipred ponderado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-159">**sinalizador de \_ bypass \_ habilitado de transquantity \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-160">**\_sinalizador habilitado para blocos \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-161">**\_ \_ sinalizador habilitado para sincronização de codificação de \_ entropia \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-162">**\_sinalizador de espaçamento uniforme \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-163">**filtro de loop \_ \_ no \_ \_ sinalizador habilitado para blocos \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-164">**filtro de loop do PPS \_ \_ \_ no \_ \_ sinalizador habilitado para fatias \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-165">**sinalizador de desbloqueio de \_ substituição de filtro \_ \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-166">**\_sinalizador de desbloqueio de filtro do PPS \_ \_ desabilitado \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-167">**\_sinalizador de modificação \_ presente \_ de lista**</span><span class="sxs-lookup"><span data-stu-id="9e975-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-168">**sinalizador de extensão de cabeçalho de segmento de fatia \_ \_ \_ \_ presente \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-169">**IrapPicFlag**</span><span class="sxs-lookup"><span data-stu-id="9e975-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-170">**IdrPicFlag**</span><span class="sxs-lookup"><span data-stu-id="9e975-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-171">**IntraPicFlag**</span><span class="sxs-lookup"><span data-stu-id="9e975-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="9e975-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-173">**dwCodingSettingPicturePropertyFlags**</span><span class="sxs-lookup"><span data-stu-id="9e975-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-174">**deslocamento do PPS \_ CB \_ QP \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-175">**deslocamento do PPS \_ CR \_ QP \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-176">**\_colunas de bloco num \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-177">**número \_ de \_ linhas de bloco \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-178">**\_minus1 de largura da coluna \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-179">**altura da linha \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="9e975-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-180">**comparação \_ cu \_ QP \_ de \_ profundidade Delta**</span><span class="sxs-lookup"><span data-stu-id="9e975-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-181">**div2 de deslocamento do PPS \_ beta \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-182">**\_div2 de \_ deslocamento de TC do PPS \_**</span><span class="sxs-lookup"><span data-stu-id="9e975-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-183">**log2 \_ de \_ nível de mesclagem paralela \_ \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="9e975-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-184">**CurrPicOrderCntVal**</span><span class="sxs-lookup"><span data-stu-id="9e975-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-185">**RefPicList**</span><span class="sxs-lookup"><span data-stu-id="9e975-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="9e975-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-187">**PicOrderCntValList**</span><span class="sxs-lookup"><span data-stu-id="9e975-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-188">**RefPicSetStCurrBefore**</span><span class="sxs-lookup"><span data-stu-id="9e975-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-189">**RefPicSetStCurrAfter**</span><span class="sxs-lookup"><span data-stu-id="9e975-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-190">**RefPicSetLtCurr**</span><span class="sxs-lookup"><span data-stu-id="9e975-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="9e975-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="9e975-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9e975-193">**StatusReportFeedbackNumber**</span><span class="sxs-lookup"><span data-stu-id="9e975-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="9e975-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9e975-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9e975-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e975-195">Requirements</span></span>



| <span data-ttu-id="9e975-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e975-196">Requirement</span></span> | <span data-ttu-id="9e975-197">Valor</span><span class="sxs-lookup"><span data-stu-id="9e975-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9e975-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e975-198">Minimum supported client</span></span><br/> | <span data-ttu-id="9e975-199">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e975-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9e975-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e975-200">Minimum supported server</span></span><br/> | <span data-ttu-id="9e975-201">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="9e975-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9e975-202">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e975-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e975-203"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e975-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e975-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e975-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e975-205">Estruturas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e975-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




