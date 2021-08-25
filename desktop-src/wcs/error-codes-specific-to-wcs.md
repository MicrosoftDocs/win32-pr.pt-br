---
title: Códigos de erro específicos do WCS
description: Veja a seguir uma lista de códigos de erro especificamente relacionados ao uso do WCS 1.0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46127e27b0f0890e305fee65534b0cce743c086e9e89934797bf2b16b15e9f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814596"
---
# <a name="error-codes-specific-to-wcs"></a>Códigos de erro específicos do WCS

Veja a seguir uma lista de códigos de erro especificamente relacionados ao uso do WCS 1.0. Isso não significa que as funções WCS retornarão apenas esses códigos de erro. Isso significa que os códigos na tabela a seguir são retornados apenas por funções WCS. Eles também podem retornar outros códigos de erro win32 documentados em outro lugar na API win32 do SDK da plataforma.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERRO \_ AO EXCLUIR ICM \_ \_ XFORM
</dt> <dd>

Não foi possível excluir a transformação de cor especificada.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>MARCAÇÃO \_ \_ DUPLICADA DE ERRO
</dt> <dd>

A marca de elemento de perfil de cor especificada já está presente no perfil de cor.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERRO \_ ICM \_ NÃO \_ HABILITADO
</dt> <dd>

O Gerenciamento de Cores de Imagem não está habilitado no momento.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERRO \_ \_ CMM INVÁLIDO
</dt> <dd>

O nome do arquivo especificado não se refere a um módulo de gerenciamento de cores válido.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERRO \_ \_ COLORSPACE INVÁLIDO
</dt> <dd>

O espaço de cores especificado é inválido.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERRO \_ PERFIL \_ INVÁLIDO
</dt> <dd>

O nome do arquivo especificado não se refere a um perfil de cor válido.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERRO \_ TRANSFORMAÇÃO \_ INVÁLIDA 
</dt> <dd>

A transformação de cor especificada não é uma transformação de cor válida.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>PERFIL \_ DE ERRO NÃO ASSOCIADO AO \_ \_ \_ \_ DISPOSITIVO
</dt> <dd>

O perfil de cor especificado não está associado a nenhum dispositivo.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>PERFIL \_ DE ERRO NÃO \_ \_ ENCONTRADO 
</dt> <dd>

O nome do arquivo de perfil de cor especificado não foi encontrado. O nome ou caminho do arquivo está incorreto.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>MARCA \_ DE ERRO NÃO \_ \_ ENCONTRADA
</dt> <dd>

A marca de elemento de perfil de cor especificada não foi encontrada no perfil de cor.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>MARCA \_ DE ERRO NÃO \_ \_ PRESENTE
</dt> <dd>

Uma marca de elemento de perfil de cor necessária para que a função tenha êxito não foi passada para a função.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Constantes do WCS](wcs-constants.md)
</dt> </dl>

 

 




