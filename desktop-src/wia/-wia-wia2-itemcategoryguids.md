---
description: Os itens de aquisição de imagem do Windows (WIA) 2,0 são agrupados em categorias que definem como um IWiaItem2 deve ser tratado ou usado.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUIDs de categoria de item WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785162"
---
# <a name="wia-20-item-category-guids"></a>GUIDs de categoria de item WIA 2,0

Os itens de aquisição de imagem do Windows (WIA) 2,0 são agrupados em categorias que definem como um [**IWiaItem2**](-wia-iwiaitem2.md) deve ser tratado ou usado. Por exemplo, se o item representa um alimentador, o aplicativo deve esperar que ele contenha as propriedades necessárias do alimentador de documentos e opere como um alimentador de documentos. Se o item representa um arquivo concluído, um aplicativo WIA 2,0 deve tratá-lo dessa forma, supondo que os dados sejam estáticos e localizados no dispositivo. (As regras para cada item serão definidas em seus documentos de especificação individuais.) Cada categoria tem uma constante de tipo GUID.



| Constante                                                                                                                                                                                               | Descrição                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**\_automático da categoria WIA \_**</dt> </dl>                             | Um item que representa as definições de configuração automática para um dispositivo de scanner WIA 2,0 que dá suporte à verificação configurada automaticamente.<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**\_alimentador de categoria WIA \_**</dt> </dl>                       | Um item do alimentador que é uma fonte de dados programável e segue as regras padrão e os conjuntos de propriedades necessários para dar suporte aos alimentadores de documentos.<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**\_voltar do \_ alimentador de categoria WIA \_**</dt> </dl>       | Uma fonte de dados programável que descreve a fonte de dados do lado de fundo de um item do alimentador base duplex.<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**\_frente do \_ alimentador de categoria WIA \_**</dt> </dl>    | Uma fonte de dados programável que descreve a fonte de dados do Front Side de um item do alimentador base duplex.<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**\_filme de categoria WIA \_**</dt> </dl>                             | Um item de filme que é uma fonte de dados programável e segue as regras padrão e os conjuntos de propriedades necessários para dar suporte a unidades de verificação de filmes.<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**\_arquivo de categoria WIA \_ concluído \_**</dt> </dl> | Um item que não é uma fonte de dados programável ou um item que fornece dados em um formato de arquivo concluído ou um item de pasta que contém itens de formato de arquivo concluído.<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**\_superfície da categoria WIA \_**</dt> </dl>                    | Um item de mesa que é uma fonte de dados programável e segue as regras padrão e os conjuntos de propriedades necessários para dar suporte à verificação do cilindro de mesa.<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**\_pasta da categoria WIA \_**</dt> </dl>                       | Um item de armazenamento de pasta (não uma fonte de dados programável) que contém outros itens de pasta ou arquivos concluídos ou ambos.<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**\_raiz da categoria WIA \_**</dt> </dl>                             | O item raiz do dispositivo. <br/>                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




