---
title: Códigos de erro específicos do WCS
description: Veja a seguir uma lista de códigos de erro que estão especificamente relacionados ao uso do WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105790673"
---
# <a name="error-codes-specific-to-wcs"></a>Códigos de erro específicos do WCS

Veja a seguir uma lista de códigos de erro que estão especificamente relacionados ao uso do WCS 1,0. Isso não significa que as funções WCS retornarão apenas esses códigos de erro. Isso significa que os códigos na tabela a seguir são retornados apenas pelas funções WCS. Eles também podem retornar outros códigos de erro do Win32 que estão documentados em outro lugar na API do Win32 do SDK da plataforma.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERRO ao \_ excluir o \_ XFORM de ICM \_
</dt> <dd>

Não foi possível excluir a transformação de cor especificada.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERRO \_ de \_ marca duplicada
</dt> <dd>

A marca do elemento do perfil de cor especificado já está presente no perfil de cores.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERRO \_ ICM \_ não \_ habilitado
</dt> <dd>

O gerenciamento de cores de imagem não está habilitado no momento.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERRO \_ \_ CMM inválido
</dt> <dd>

O nome de arquivo especificado não se refere a um módulo de gerenciamento de cores válido.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERRO \_ \_ COLORSPACE inválido
</dt> <dd>

O espaço de cores especificado é inválido.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERRO \_ de \_ perfil inválido
</dt> <dd>

O nome de arquivo especificado não se refere a um perfil de cor válido.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>\_transformação inválida de erro \_ 
</dt> <dd>

A transformação de cor especificada não é uma transformação de cor válida.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_perfil \_ de erro não \_ associado \_ ao \_ dispositivo
</dt> <dd>

O perfil de cor especificado não está associado a nenhum dispositivo.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>Perfil de erro \_ \_ não \_ encontrado 
</dt> <dd>

O nome do arquivo do perfil de cor especificado não foi encontrado. O nome do arquivo ou o caminho está incorreto.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>marca de erro \_ \_ não \_ encontrada
</dt> <dd>

A marca do elemento de perfil de cor especificado não foi encontrada no perfil de cor.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>marca de erro \_ \_ não \_ presente
</dt> <dd>

Uma marca de elemento de perfil de cor que é necessária para que a função tenha êxito não foi passada para a função.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Constantes do WCS](wcs-constants.md)
</dt> </dl>

 

 




