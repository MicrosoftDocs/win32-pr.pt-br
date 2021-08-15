---
description: As constantes a seguir são usadas com o protocolo COPP (certificado de proteção de saída) para mecanismos de proteção de saída específicos.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Sinalizadores de tipo de proteção COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 75038b22a30be41389311fd1a7cfb830f870859b01ba48fd9a791a42cee86dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214046"
---
# <a name="copp-protection-type-flags"></a>Sinalizadores de tipo de proteção COPP

As constantes a seguir são usadas com o protocolo COPP (certificado de proteção de saída) para mecanismos de proteção de saída específicos.



| Constante/valor                                                                                                                                                                                                                                                                                                             | Descrição                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**Copp \_ ProtectionType \_ desconhecido**</dt> <dt>0x80000000</dt> </dl>     | Mecanismo de proteção desconhecido.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**Copp \_ ProtectionType \_ nenhum**</dt> <dt>0x00000000</dt> </dl>                 | Nenhum mecanismo de proteção.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**Copp \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth Proteção de Conteúdo Digital (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**Copp \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Proteção de cópia analógica (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**Copp \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | Sistema de gerenciamento de geração de cópia analógico (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**Copp \_ ProtectionType \_ máscara**</dt> <dt>0x80000007</dt> </dl>                 | Bitmask para isolar sinalizadores válidos.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**Copp \_ Proteção 0x7FFFFFF8 \_ reservada**</dt> <dt></dt> </dl> | Reservado. Deve ser zero.<br/>                              |



## <a name="remarks"></a>Comentários

Alguns métodos retornam um único sinalizador desse tipo de enumeração, e alguns métodos retornam **uma operação OR de um ou mais** sinalizadores.

Esses sinalizadores são usados nas consultas e comandos de COPP a seguir.

-   Nível de proteção global
-   Nível de proteção local
-   Tipo de proteção
-   Definir nível de proteção

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




